# Real-Time ASL Recognition System

A real-time American Sign Language (ASL) recognition system built with MediaPipe hand landmarks and a fully connected neural network (FCNN). The project captures live hand movement through a webcam, extracts meaningful spatial features from the hand, and predicts ASL letters in real time.

## Introduction

This repository demonstrates how computer vision and deep learning can be combined to build an interactive sign-language recognition application. The system is designed for educational and experimental use, and it provides a practical example of how MediaPipe can be used to extract hand landmark data that is then classified by a neural network.

The main goal of this project is to turn hand gestures into recognized ASL symbols using a lightweight and efficient pipeline that can run in real time on a standard laptop or desktop computer.

## Demo

<img width="788" height="624" alt="Untitled" src="https://github.com/user-attachments/assets/4a914ee0-1cab-42cd-938b-8a41499dc0ad" />


## Overview

This repository contains the full workflow for building and running an ASL recognition system:

- Collect or prepare datasets of ASL hand images
- Extract hand landmark features using MediaPipe
- Split the data into training and testing sets
- Train a fully connected neural network classifier
- Run live inference from a webcam in real time

## Key Features

- Real-time hand tracking using MediaPipe Hand Landmarker
- Landmark-based classification for ASL letters
- Fast and lightweight FCNN model for inference
- Notebook-based workflow for data preparation, training, and testing
- Support for webcam-based live prediction

## Project Structure

- `extract_landmarks_dataset.ipynb` — prepares the dataset and extracts hand landmarks
- `train_mediapipe_model.ipynb` — trains the neural network model
- `land_webcam.ipynb` — runs live webcam inference
- `split_dataset.ipynb` — splits data into training and testing sets
- `requirements.txt` — Python dependencies
- `mediapipe_labels_handedness_fixed.json` — label mapping used by the project
- `mediapipe_model_handedness_fixed.keras` — pre-trained model file

## Requirements

The project requires Python 3.10+ and the packages listed in `requirements.txt`.

Install the dependencies with:

```bash
pip install -r requirements.txt
```

## Getting Started

### 1. Prepare the dataset
Open and run `extract_landmarks_dataset.ipynb` to process your ASL image dataset and extract hand landmarks.

### 2. Train the model
Open and run `train_mediapipe_model.ipynb` to train the FCNN classifier using the extracted features.

### 3. Run real-time inference
Open and run `land_webcam.ipynb` to start the webcam demo and view predictions live.

## Model Details

The system uses:

- MediaPipe Hand Landmarker for hand detection and landmark extraction
- A fully connected neural network for classification
- ASL letter labels ranging from `A` to `Z`

## Notes

- The trained model file is included as `mediapipe_model_handedness_fixed.keras`
- The label list is defined in `mediapipe_labels_handedness_fixed.json`
- For best results, use clear lighting and keep the hand visible within the camera frame
- This project is best suited for experimentation, learning, and prototype development

## Future Improvements

Possible enhancements include:

- Support for more ASL words and phrases
- Improved accuracy with larger datasets
- Better handling of hand orientation and occlusion
- Deployment as a web app or mobile application

## License

This project is distributed for educational and research purposes.
