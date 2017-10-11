# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go. The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle. Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project I detected lane lines in images using Python and [OpenCV](http://opencv.org/) (Open-Source Computer Vision).


The pipeline
---

1. Apply the Grayscale transform to return the image with only one color channel
2. Apply a Gaussian Noise kernel to get rid of some noises
3. Apply the [Canny transform](https://en.wikipedia.org/wiki/Canny_edge_detector) to detect edges
4. Apply an image mask so that only the region of interest is selected
5. Apply the [Hough transform](https://en.wikipedia.org/wiki/Hough_transform) to draw hough lines
6. Connect the lines
7. Plot the lines on top of the original image


### Solid White Right
[![Solid White Left](https://github.com/zhoujh30/CarND-LaneLines-P1/blob/master/white.gif?raw=true)](https://youtu.be/TrcnszzbVkM)
### Solid Yellow Left
[![Solid Yellow Left](https://github.com/zhoujh30/CarND-LaneLines-P1/blob/master/yellow.gif?raw=true)](https://youtu.be/Zmi22-l1W6I)



Shortcomings
---


Possible Improvements
---

 
