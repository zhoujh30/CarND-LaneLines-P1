# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go. The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle. Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project I detected lane lines in images using Python and [OpenCV](http://opencv.org/) (Open-Source Computer Vision).


The pipeline
---
(For details, please see [Jupyter Notebook](https://github.com/zhoujh30/CarND-LaneLines-P1/blob/master/P1.ipynb))

1. Apply the Grayscale transform to return the image with only one color channel

2. Apply a Gaussian Noise kernel to get rid of some noises

3. Apply the [Canny transform](https://en.wikipedia.org/wiki/Canny_edge_detector) to detect edges

4. Apply an image mask so that only the region of interest is selected

5. Apply the [Hough transform](https://en.wikipedia.org/wiki/Hough_transform) to draw hough lines

6. Connect the lines

    A. Split lines by slope into right and left lines
    
    B. Average the slope and intercept of the lines
    
    C. Generate new start and end points for averaged lines
    
    D. Connect the lines

7. Plot the lines on top of the original image

8. Apply all steps above to the videos

#### Solid White Right
[![Solid White Left](https://github.com/zhoujh30/CarND-LaneLines-P1/blob/master/white.gif?raw=true)](https://youtu.be/TrcnszzbVkM)
#### Solid Yellow Left
[![Solid Yellow Left](https://github.com/zhoujh30/CarND-LaneLines-P1/blob/master/yellow.gif?raw=true)](https://youtu.be/Zmi22-l1W6I)



Shortcomings
---
1. Static region of interest in image masking might not work for all scenarios, e.g. driving on curve roads
2. Canny edge detection and lines connection don't work very well on lighter-colored roads with low contrast between lane color and road color


Possible Improvements
---
1. Apply neural network to image masking to select a dynamic region of interest that learns to work for all scenarios
2. Employ additional tools to help improve edge detection and lines connection
 
