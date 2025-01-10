# Automated Coin Detection and Counting

In an increasingly digitized world where automation and efficiency are paramount, the problem of automated coin detection and counting holds profound significance. This project aims to develop algorithms and systems capable of accurately identifying, localizing, and quantifying coins within digital images. Applications span diverse sectors, including retail, finance, robotics, and assistive technology. 

This project focuses on creating a Python program for coin detection in images, utilizing advanced techniques from computer vision and image processing.

## Project Overview

The provided code captures video from a phone's camera, processes each frame to detect contours, and estimates the total amount of money based on the characteristics of the detected contours, such as area and shape. Below is a concise explanation of the code structure and some suggested improvements for better performance.

### Imports and Initialization

- Import necessary libraries:
  - `cv2` for OpenCV functionalities
  - `numpy` for numerical operations
  - `cvzone` for high-level image processing functionalities
- Initialize global variables, such as `totalMoney`, a `ColorFinder` instance, and the HSV values for color detection.

### Preprocessing Function

- The preprocessing function performs the following steps:
  - Converts an image to grayscale
  - Applies Gaussian blur
  - Detects edges using the Canny method
  - Performs morphological operations to enhance the edges

### Main Loop for Video Capture

- Capture video from the phone's camera using its IP address.
- Read frames in a loop, preprocess them, and find contours.
- Classify contours based on their area and circularity to identify different denominations of money, updating the total amount as necessary.
- Display the processed image with the detected contours and the total money overlaid.
- Exit the loop when the 'q' key is pressed.

### Important Note

Adjust the area size of the detected coins according to your preferences; failing to do so may lead to inaccurate results.

## Getting Started

To run the project, ensure you have the required libraries installed. You can install them via pip:

```bash
pip install opencv-python numpy cvzone
```

Then, run the main script, and follow the instructions to connect your phone's camera.
