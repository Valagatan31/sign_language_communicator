# Project Overview

This project presents a Vision-Based Indian Sign Language (ISL) Recognition System using Deep Learning.
The system captures hand gestures from video input, extracts hand landmarks using MediaPipe, and classifies gestures using Bi-LSTM and X3D models.

The goal is to reduce communication barriers between deaf individuals and non-signers.

# Objectives
- Recognize ISL gestures from video input
- Convert gestures into text
- Build a low-cost vision-based system
- Compare CNN, LSTM, Bi-LSTM, and X3D models
- Improve generalization using custom dataset

# model used 
- ResNet18
- AlexNet
- mdiapipe
- Rnn
- biLstm
- x3d

# Technologies Used
- Python
- OpenCV
- MediaPipe
- PyTorch
- NumPy
- Pandas
- Jupyter Notebook
- VS Code

# Methodology
- Video Data Collection
- Frame Extraction (OpenCV)
- Landmark Extraction (MediaPipe)
- Feature Conversion (NumPy arrays)
- Model Training (Bi-LSTM / X3D)

# Results
- Mediapipe + Bi-LSTM achieved 97.75% training accuracy and 50% validation accuracy.
- X3D achieved 97.75% training and 89% validation accuracy.



# Future work
- Increase dataset size
- Add more ISL signs
- Implement real-time recognition
- Convert text back to sign language
- Deploy as web/mobile app





