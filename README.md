# Face Detection using Laptop Camera

This project demonstrates real-time face detection using OpenCV and MediaPipe libraries. The application captures video from the laptop's camera, detects faces, and draws bounding boxes around detected faces. Additionally, it displays the confidence score for each detection and the total number of faces detected in the current frame.

## Table of Contents
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Customization](#customization)

## Features
- Real-time face detection using the laptop camera.
- Bounding boxes drawn around detected faces.
- Confidence scores displayed for each detection.
- Total number of faces displayed on the screen.
- Uses MediaPipe for face detection and OpenCV for video capture and processing.

## Requirements
Before running the project, ensure you have the following installed:
- Python 3.x
- OpenCV (`opencv-python`)
- MediaPipe (`mediapipe`)

## Installation
1. Clone the repository or download the project files:
    ```bash
    git clone https://github.com/ashwindalvi300/Face-Detection-using-Laptop-Camera.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Face-Detection-using-Laptop-Camera
    ```

3. Install the required libraries using `pip`:
    ```bash
    pip install opencv-python
    pip install mediapipe
    ```

## Usage
1. Run the Python script to start face detection using your laptop's camera:
    ```bash
    python face_detection.py
    ```

2. The program will open a window showing the camera feed with bounding boxes around detected faces, the detection confidence, and the total number of faces in the frame.

3. To stop the face detection, press the **'q'** key.

## How It Works
- **OpenCV**: Used for capturing video from the camera and for image processing (drawing rectangles, putting text, etc.).
- **MediaPipe**: Provides a pre-trained face detection model. It processes each frame to detect faces and returns bounding box coordinates and confidence scores.

### Key Components
1. **Video Capture**: The camera feed is captured using `cv2.VideoCapture(0)`, where `0` specifies the default camera.
2. **Face Detection**: The `MediaPipe` face detection model is initialized with a confidence threshold of 60%. Detected faces are outlined with red rectangles, and their confidence scores are displayed.
3. **Real-time Display**: The faces detected are displayed in real-time, with the ability to press 'q' to exit the program.

## Customization
- **Confidence Threshold**: You can modify the face detection confidence threshold by changing the parameter `FaceDetection(0.6)` in the script to a different value (0 to 1).
- **Camera Source**: If you have multiple cameras, change `cv2.VideoCapture(0)` to `cv2.VideoCapture(1)` (or other numbers) to use a different camera.
- **Frame Rate**: Adjust the frame processing speed by modifying the `cv2.waitKey(1)` delay value.




