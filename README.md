# Semiconductor Chip Hotspot Detection using CNN

This project implements a deep learning-based image classification system to detect hotspots (defective regions) in semiconductor chip layouts. The model is trained on real chip layout images and deployed for predicting potential manufacturing defects.

# Motivation

Semiconductor manufacturing is highly sensitive to defects during photolithography. Detecting hotspots (regions prone to defects) early in the design process helps in preventing costly failures in chip fabrication. Traditional rule-based approaches struggle with complex patterns, hence the use of deep learning for accurate hotspot detection.

By utilizing Convolutional Neural Networks (CNN), this project aims to provide an automated and scalable solution to identify hotspots in VLSI design layouts.

# Dataset

The dataset is sourced from the ICCAD Benchmark Suite, consisting of labeled layout images:

Classes: Hotspot and Non-Hotspot

Preprocessing:

Images resized to 128x128

Data split into train (70%), validation (20%), and test (10%)

Data augmentation applied (horizontal and vertical flips)

# Project Pipeline

1.Data Preparation

Image loading and splitting using splitfolders

Augmentation with ImageDataGenerator

2.Model Development

CNN model using Conv2D, MaxPooling2D, Flatten, Dense, Dropout

Binary classification with sigmoid activation

Compiled with Adam optimizer and binary cross-entropy loss

3.Training and Evaluation

Trained for 10 epochs on augmented data

Validated on unseen layout images

Evaluated using accuracy and loss metrics

Deployment (Optional)

Model saved using joblib or keras.models.save_model

Flask API to serve predictions

Dockerized and deployed via AWS or local container

# Results

Validation Accuracy: ~95%

Loss: Reduced significantly over epochs, showing good learning

Prediction Mechanism: Each image classified as Hotspot or Non-Hotspot, enabling automated layout screening

