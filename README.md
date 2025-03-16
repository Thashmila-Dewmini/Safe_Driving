# Eye Detection and Drowsiness Detection

## Overview
This project uses OpenCV and Dlib to detect eyes and analyze the Eye Aspect Ratio (EAR) to determine if a person is drowsy, sleepy, or sleeping based on facial landmarks.

## Features
- Detects eyes using Haar cascades.
- Uses Dlib's facial landmarks to compute EAR.
- Classifies eye states as "Open," "Drowsy," "Near Sleep," or "Sleeping."
- Provides visual alerts on screen.

## Requirements
Make sure you have the following dependencies installed:
```bash
pip install opencv-python dlib numpy scipy
```
Additionally, you need the `shape_predictor_68_face_landmarks.dat` file from Dlib. Download it from:
[https://github.com/davisking/dlib-models](https://github.com/davisking/dlib-models)

## How to Run
1. Ensure your webcam is connected.
2. Run the script:
   ```bash
   python EyeDetection.py
   ```
3. Press `q` to exit the program.

## Eye Aspect Ratio (EAR) Thresholds
- **EAR > 0.26**: Eyes Open
- **0.20 < EAR < 0.26**: Drowsy
- **0.18 < EAR < 0.20**: Near Sleep
- **EAR < 0.18**: Sleeping

