# ✋ Real-Time Hand Gesture Recognition & Touchless Control

A real-time hand gesture recognition system that uses **MediaPipe Hands, OpenCV, TensorFlow/Keras, and TensorFlow Lite** to recognize hand gestures and enable touchless interaction.

The system extracts hand landmarks from a camera stream, engineers geometric features, classifies gestures using a machine-learning model, and provides a TensorFlow Lite model for lightweight Android deployment.

---

## 🚀 Project Overview

This project implements a computer-vision-based gesture recognition pipeline for touchless human-computer interaction.

The system:

- Captures hand movements using a camera
- Detects 21 hand landmarks using MediaPipe
- Extracts geometric features from the landmarks
- Uses a trained TensorFlow/Keras model to classify gestures
- Converts the model to TensorFlow Lite
- Provides Android-ready inference assets
- Maps recognized gestures to application actions

---

## ✨ Features

- 📷 Real-time camera-based hand detection
- ✋ 21-point hand landmark extraction
- 🧠 Machine-learning-based gesture classification
- 📐 Hand geometry feature extraction
- 🔄 Gesture data augmentation
- 📊 Model evaluation and confusion matrix
- 📱 TensorFlow Lite deployment
- ⚡ Quantized TFLite model for lightweight inference
- 🤖 Android integration support
- 🖥️ Touchless presentation interaction
- 🎵 Touchless music interaction

---

## 🏗️ System Architecture

```text
        Camera / Webcam
               │
               ▼
     ┌────────────────────┐
     │   MediaPipe Hands  │
     │  21 Hand Landmarks │
     └─────────┬──────────┘
               │
               ▼
     ┌────────────────────┐
     │ Feature Extraction │
     │                    │
     │ • Raw landmarks    │
     │ • Joint angles     │
     │ • Tip distances    │
     │ • Hand geometry    │
     └─────────┬──────────┘
               │
               ▼
     ┌────────────────────┐
     │  StandardScaler    │
     │ Feature Normalization
     └─────────┬──────────┘
               │
               ▼
     ┌────────────────────┐
     │ TensorFlow / Keras │
     │ Gesture Classifier │
     └─────────┬──────────┘
               │
               ▼
     ┌────────────────────┐
     │ TensorFlow Lite    │
     │ Lightweight Model  │
     └─────────┬──────────┘
               │
               ▼
     ┌────────────────────┐
     │ Application Actions│
     │ Presentation/Music │
     └────────────────────┘
