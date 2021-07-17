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

The pipeline starts with the conversion of the color image to a gray image. After this step, a gaussian blur filter with a kernel size of 3 is applied to the gray image to remove noise. Then the edges are detected with the Canny edge detection. As threshold values were 60 for the lower and 150 for the upper was chosen. The result of the edge detection works well as we can see in ![alt text][image1].

### 2. Identify potential shortcomings with your current pipeline





### 3. Suggest possible improvements to your pipeline

