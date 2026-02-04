# Problem Statement

Public ISL datasets often contain very limited variation (sometimes a single video per word). Models trained on such data overfit and fail to generalize to new people and environment

# Overview

Indian Sign Language (ISL) recognition from videos is challenging due to dataset scarcity and signer variability. Initial experiments on existing datasets led to overfitting and poor real-world performance.

To address this, we created a custom dataset with multiple individuals performing selected signs. Instead of using full frames, we used MediaPipe to extract hand landmarks only, so the model learns pure gesture dynamics. After testing multiple architectures, the best results came from fine-tuning a pretrained X3D model for spatio-temporal understanding.

# Custom Dataset

Signs (6): Hello, Namaste, Good Morning, Headache, Happy, Beautiful

15 videos per sign

Multiple people per sign

Testing on 10 unseen individuals

# Hand Landmark Extraction (MediaPipe)
Removed background noise

Reduced input size

Focused only on hand motion for better learning

# Model Evolution
Model	Issue
ResNet18 + BiLSTM	Overfitting (full frames, noisy background)
AlexNet + BiLSTM	Still overfitting
MediaPipe + BiLSTM	Accuracy improved
X3D (pretrained) fine-tuned	Best accuracy & generalization

# Final Model — X3D for Video Understanding
Captures motion across frames

Lightweight and powerful for video tasks

Best performance in our experiments

# Tech Stack

Python, OpenCV

MediaPipe

PyTorch / PyTorchVideo

BiLSTM

X3D (pretrained)

# Key Learnings

Dataset variation > model complexity

Background removal improves accuracy

Pretrained video models generalize better for gestures

# Future Work

Add more ISL signs

Real-time webcam integration

Text-to-speech output

Web/mobile deployment for accessibility



