# **Finding Lane Lines on the Road** 

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidYellowCurve.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 7 steps.
1) Coverting the images to grayscale
2) Applying a Gaussian blur to the images
3) Applying Canny edge detection
4) Masking the images so that only the region of interest is processed
5) Running the Hough transform to identify lines
6) Smoothikng the result with a average slope and intercept of each side lines
7) Ploting the lines on top of the images

In order to draw a single line on the left and right lanes, I modified the draw_lines() function as follows:
1) Calculate the averge slopes and intercepts for left lines and right lines
2) Extrapolate each of the lines to the top and bottom of the lane

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


My current pipeline works well on the first two videos, but I am getting a float infinity error on the optinal third video. I will solve this issue after I get necessary knowledge for this issue.


### 3. Suggest possible improvements to your pipeline

I'd like to get better parameters for Hough transform, so I need to get more knowlege for rho and theta values.
