# Snake Scale Counting Using Contour Detection

This repository contains the code and methodology for counting snake scales using computer vision techniques. We explore two distinct approaches: one relying heavily on preprocessing and manual cropping followed by edge detection, and another using image segmentation.

## Overview

Snake scale counting is a challenging task due to the variations in scale sizes, orientations, and image quality. Our goal is to automate this process using contour detection and segmentation methods to accurately count scales on snake images.

## Approaches

### 1. Preprocessing & Edge Detection
- **Manual Cropping**: The region of interest (ROI) is manually cropped from the image to isolate the snake's body.
- **Grayscale Conversion**: The cropped image is converted to grayscale to reduce complexity and remove color noise.
- **Gaussian Blur**: A Gaussian blur filter is applied to smooth the image and reduce noise, making edge detection more effective.
- **Edge Detection**: We use the Canny edge detection algorithm to identify the boundaries of the scales.
- **Contour Detection**: Contours are extracted from the detected edges and analyzed to estimate the number of scales.

### 2. Segmentation-Based Approach
- **Automatic Segmentation**: In this approach, we bypass manual cropping by using a segmentation model to automatically identify the snake's body within the image.
- **Contour Detection**: Once the snake is segmented, contours are detected directly from the segmented image without the need for additional preprocessing.
- **Scale Counting**: The contours are analyzed to count the scales on the segmented portion of the snake.

## Tech Stack

- **Programming Language**: Python
- **Libraries & Tools**:
  - OpenCV: For image processing, edge detection, and contour detection
  - NumPy: For numerical computation
  - Matplotlib: For visualizing results
