# American Sign Language (ASL) Alphabet Recognition

![Python](https://img.shields.io/badge/Python-3.12-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## Project Overview

This project is a **Convolutional Neural Network (CNN)** based system for recognizing **American Sign Language (ASL) alphabets** from images. The model is trained on a dataset of 87,000 images spanning 29 classes (A–Z + SPACE, DELETE, NOTHING).  

The system can be used for **real-time ASL interpretation**, assisting communication between deaf/mute individuals and others.

---

## Dataset

- **Source:** [ASL Alphabet Dataset](https://www.kaggle.com/grassknoted/asl-alphabet)
- **Training set:** 87,000 images, 200x200 pixels
- **Classes:** 29 (26 letters + 3 extra classes)
- **Test set:** 29 images for real-world testing
- **Split:** 80% training, 20% validation, separate test set

### Preprocessing Steps

- Resize images to 128×128 pixels
- Normalize pixel values to [0,1]
- One-hot encode class labels
- Apply data augmentation for training:
  - Random rotation ±15°
  - Width/height shift ±10%
  - Zoom ±10%
  - Horizontal flipping

---

## Features

- CNN with 3 convolutional blocks + fully connected layers
- Batch normalization and dropout to prevent overfitting
- Early stopping and learning rate reduction
- Performance evaluation: Accuracy, Precision, Recall, F1-score, Confusion Matrix

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/<your-username>/ASL-Alphabet-Recognition.git
cd ASL-Alphabet-Recognition
