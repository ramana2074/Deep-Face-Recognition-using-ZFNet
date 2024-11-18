# Deep Face Recognition using ZFNet-Inspired Model

This project implements a face recognition system using a simplified ZFNet-inspired architecture, optimized for performance and accuracy. It aligns with the methodology discussed in the paper **"Deep Face Recognition based on an Optimized Deep Neural Network using ZFNet"**.

---

## Project Overview

The model architecture is inspired by ZFNet, leveraging convolutional neural networks (CNNs) for image classification. It has been tailored and optimized for face recognition, achieving high validation accuracy with a compact and efficient design.

---

## Features
- **ZFNet-Inspired Architecture**: The network design is based on ZFNet principles, focusing on feature extraction with convolutional layers.
- **Optimized Training Pipeline**: Includes data augmentation and adaptive learning rate adjustments.
- **High Accuracy**: Achieved a validation accuracy of **96.67%** with 15 face classes.
- **Callbacks for Efficiency**:
  - Learning rate scheduler to dynamically reduce the learning rate on plateau.
  - Early stopping to prevent overfitting.

---
## Dataset
The database contains 165 GIF images of 15 subjects (subject01, subject02, etc.).  There are 11 images per subject, one  for each 
of the following facial expressions or configurations: center-light, w/glasses, happy, left-light, w/no glasses, normal, right-light, 
sad, sleepy, surprised, and wink.  Note that the image "subject04.sad" has been corrupted and has been substituted by "subject04.normal".
Dataset : https://www.kaggle.com/datasets/olgabelitskaya/yale-face-database/data
## Model Architecture
The ZFNet-inspired model consists of:
1. **Convolutional Layers**: 
   - Feature extraction using varying kernel sizes: `7x7`, `5x5`, and `3x3`.
   - Activation: ReLU.
2. **Pooling Layers**: Max pooling layers for spatial dimension reduction.
3. **Fully Connected Layers**:
   - Dense layers for classification with dropout regularization.
   - Output layer with a softmax activation for multi-class classification.

---

## Training Configuration
- **Optimizer**: Adam optimizer with a learning rate of `1e-4`.
- **Loss Function**: Categorical cross-entropy.
- **Metrics**: Accuracy.
- **Hyperparameters**:
  - Epochs: 45
  - Batch Size: 16



## Setup and Usage
### Prerequisites
Install the required Python packages:
```bash
pip install tensorflow

