# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied Gaussian Blur to the grayscaled image. And then I used Canny transform to transform the image into white and black contrast regions. Furthermore, I applied a region of interest in between (450, 325) and (520, 325) to the image to narrow down to just the white and vlack contrasts relating to the roads. After this I applied Hough transforms and applied red lines to track the roads on the image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by making the slope Boundaries [0.43, 1.0] And then I used the fraw line polytfit function to separate out the coordinates

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the car changes lanes. At that point I do not know how the lane detection adjusts itself.

Another shortcoming could be a sharp turn. Since these were almost straight lines it was east to find the region of interest. But in case of sharp turns it would be difficult to use this.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to add code to detect lanes at the time of changing lanes

Another potential improvement could be to ...
