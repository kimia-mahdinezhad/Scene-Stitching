# Scene Stitching
### In this document, we will implement the Feature Selection operation and create a panorama image using the SIFT algorithm.

## Overview
We will use OpenCV and Python to implement the SIFT operator for finding interest points, establishing correspondences between images, and matching and aligning different views of a scene with SIFT features.

## Steps
The following steps provide the required code functions and explain them thoroughly.
1.  Run the Feature Selection algorithm to obtain Point Keys and Descriptors for selected images.
2.  Find common Point Key points between two images (Vector-Based view).
3.  Calculate the Homography matrix.
4.  Seamlessly stitch two pictures together.

The following algorithms and steps are used in each section:
1.  Implement the SIFT algorithm as a Feature Selection algorithm.
2.  Find common points using BFMatcher and knnMatch.
3.  Calculate the Homography matrix with RANSAC implementation.
4.  Stitch two images using the Homography matrix, and create a mask to separate the left, middle, and right parts of the image, constructing each one separately.

To connect three images, we first combine the right and middle images, then the middle and left images separately, and finally, we merge the two resulting images together.

## Results
In the results viewing section, we observe the result of selecting features and common features between two images and finally the panoramic image for training images and images taken by my own camera.

First, we observe the given educational pictures side by side.
![](https://i.ibb.co/HXR39vT/1-1.png)

In the following, we see the selected features on each image in each step.
![](https://i.ibb.co/vJZsZGk/1-2.png)
![](https://i.ibb.co/Smxgd1r/1-3.png)
![](https://i.ibb.co/YBH2MY8/1-4.png)

Then we see the matched features between the images.
![](https://i.ibb.co/7r1kLv4/1-5.png)

Now we see the results of panoramic images.
![](https://i.ibb.co/QXXry35/1-6.png)

As can be seen, the algorithm has well selected many features as Match and the panoramic image is well made in the third stage.


In the following, we observe the pictures taken by my own camera and apply the algorithm on it as well.
![](https://i.ibb.co/6vtqcH9/1-7.png)
![](https://i.ibb.co/dWvJ107/1-8.png)

As we can see, the algorithm works well in the low light environment and has stitched the images together.
