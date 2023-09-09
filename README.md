# QR-code-distance-calculator
# Summer 2023 Research: Furthest Distance QR Code Detection

![QR Code](qr_code_image.jpg)

## Overview

Welcome to the GitHub repository for the Summer 2023 research project focused on detecting the furthest distance at which a QR code can be recognized by a webcam. This project explores the intersection of computer vision, face detection, and QR code recognition using the OpenCV library.

## Abstract

Computer vision has rapidly evolved into a critical technology with applications ranging from healthcare to entertainment. This project leverages OpenCV to address the challenge of determining the maximum distance at which a QR code can be detected by a webcam. The approach combines face detection and QR code recognition, showcasing the adaptability and integration potential of OpenCV in practical applications.

## Introduction

Computer vision is a groundbreaking technology with diverse applications, including medical image processing, mask detection, and theft prevention. In this project, we aim to determine the furthest distance at which QR codes of different sizes (2x2 and 4x4) can be detected by a laptop camera.

## OpenCV

OpenCV, a powerful open-source computer vision library, is instrumental in this project. It offers a comprehensive suite of tools and over 2500 optimized algorithms for various computer vision tasks. OpenCV's flexibility and permissive Apache 2 license make it accessible to developers and companies alike.

![Face Detection](face_detection.png)

We utilize OpenCV for face detection, which is crucial for measuring the distance between the user's face and the camera. Multiple user images are captured and stored in the `Capture_Reference_image` folder, allowing us to establish a reference for distance calculation.

## Structure of Capture_Reference_Image.py

The `Capture_Reference_Image.py` script captures user images and stores them in a directory. It uses the `cv2` library to access the camera, ensuring accurate measurement of the face's distance from the camera. When capturing an image, the user's distance from the camera is documented using a measuring tape placed at face level.

## Distance.py

The `Distance.py` script calculates the distance of a QR code from the camera. This distance is inferred from the distance of the user's face from the camera since both are at the same distance when scanning the QR code. The script employs Haar cascades for face detection and integrates OpenCV for QR code detection.

## Results

We conducted tests with 2x2 and 4x4 QR codes to determine the furthest detection distance. The results indicate a clear relationship between QR code size and the furthest detection distance.

| QR Code Size | Furthest Detection Distance |
|--------------|-----------------------------|
| 2x2          | 52.2 cm                     |
| 2x2          | 41.7 cm                     |
| 2x2          | 43.9 cm                     |
| 2x2          | 42.5 cm                     |
| 2x2          | 42.1 cm                     |
| 2x2          | 44.6 cm                     |
| 2x2          | 40.8 cm                     |
| 4x4          | 87.8 cm                     |
| 4x4          | 86.2 cm                     |
| 4x4          | 89.5 cm                     |
| 4x4          | 91.3 cm                     |
| 4x4          | 87.8 cm                     |
| 4x4          | 94.2 cm                     |
| 4x4          | 88.7 cm                     |

These results show that as the QR code size doubles, the detection distance also increases proportionally.

## Conclusion

This project demonstrates the versatility of computer vision, particularly using OpenCV, for face detection and distance estimation. By combining these techniques with QR code detection, we successfully determined the maximum distance at which a QR code can be recognized by a camera. The results confirm a consistent ratio between QR code dimensions and the furthest detection distance, validating the accuracy of our approach.

## Work Cited

- [OpenCV About](https://opencv.org/about/)
- [Bengio, Y. (2018) - Image of people’s faces](https://towardsdatascience.com/facial-keypoints-detection-deep-learning-737547f73515)
- [Cascade Classifier - OpenCV](https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html)
- [Dev, P. (2020) - Important Libraries of OpenCV](https://medium.com/javarevisited/important-libraries-of-opencv-56b14705bf0e)
