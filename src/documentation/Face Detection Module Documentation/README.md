# Face Detection Module Documentation

This module encompasses a range of functionalities aimed at detecting faces and eyes using different models and classifiers. Here is a comprehensive breakdown of the features provided:

## Features

### 1. Face Detection using Haar Cascades:
- Utilizes Haar cascade classifier to detect faces in the given image.
- Highlights detected faces in red on the image.

### 2. Cropping Face using Haar Cascades:
- Uses Haar cascade classifier to detect and crop the face from the given image.
- This feature is available only for one-person pictures.

### 3. Face Detection using LBP (Local Binary Pattern):
- Leverages LBP cascade classifier to detect faces in the given image.
- Highlights detected faces in blue on the image.

### 4. Cropping Face using LBP:
- Utilizes LBP cascade classifier to detect and crop the face from the given image.
- This feature is available only for one-person pictures.

### 5. Improved Face Detection using LBP:
- Employs an improved LBP cascade classifier for face detection in the given image.
- Highlights detected faces in yellow on the image.

### 6. Cropping Improved Face Detection using LBP:
- Uses the improved LBP cascade classifier to detect and crop the face from the given image.
- This feature is available only for one-person pictures.

### 7. Eye Detection:
- Applies Haar cascade classifiers to first detect faces, then eyes within those faces.
- Highlights detected eyes in green on the image.

### 8. Landmark Detection:
- Detects face landmarks using a pre-trained model on the given image.
- Highlights specific landmarks like the center of the nose.

## Usage

Each functionality within this module utilizes external XML files containing pre-trained models or classifiers. These classifiers are employed to detect facial features on grayscale versions of the input images. Detected features are either highlighted or cropped, and the modified image is displayed back to the user.

This module provides a robust set of face and eye detection features using different detection techniques and models, which can be instrumental in various applications such as face recognition, facial feature analysis, or image editing tools.

## External Files

The external XML files containing the pre-trained models or classifiers are essential for the operation of this module. Ensure these files are placed in the correct directory path as specified in the code for the module to function as expected.

