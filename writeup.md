# **Finding Lane Lines on the Road** 

## Writeup 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report



---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.


[//]: # (Image References)

[image1]: ./images_output/edge.png "Edge detection"
[image2]: ./images_output/lane_detection.png "Final result of lane detection"
[image2]: ./images_output/lane_detection_with_segmentation.png "Final result of lane detection with segmentation"

The pipeline starts with the conversion of the color image to a gray image. After this step, a gaussian blur filter with a kernel size of 3 is applied to the gray image to remove noise. Then the edges are detected with the Canny edge detection. As threshold values were 60 for the lower and 150 for the upper was chosen. The result of the edge detection works well as we can see in the result:

![alt text][image1].

After the edges detection, the image is masked with a polygon to obtain the region of interest for the next processing steps.
Then next processing step is find the lines in the images with the edges.

Then the next processing step is to find the lines in the images with the edges. Therefore the Hough line transform was used. As parameters for the Hough transform a $ \rho $ of 7 and $ \theta $ of 1°.``` \theta ```
Since there are short lane markers, the minimum line length is set to 2, to detect them. The line gap parameter is 10. There are two implementations to draw the lines, the draw_lines and draw_lines_ext. The draw_lines function draws the found lines with Hough transformation into the image. 
The result of the this drawing functions can be observed in this image:
![alt text][image2].

### 2. Identify potential shortcomings with your current pipeline





### 3. Suggest possible improvements to your pipeline

