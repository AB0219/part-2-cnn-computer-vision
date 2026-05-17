# CNN-Based Manufacturing Defect Detection

## Project Overview

This project demonstrates a Convolutional Neural Network (CNN) based computer vision solution for detecting manufacturing defects from product surface images.

The system classifies images into four categories:

- normal
- scratch
- dent
- stain

The project showcases how CNNs can automatically learn visual patterns from images and perform defect classification with high accuracy.


# Problem Statement

Manufacturing industries require automated quality inspection systems to identify defective products efficiently.

In this project, a CNN model is trained to classify product images into different defect categories using image classification techniques.


# Computer Vision Problem Type

## Image Classification

This dataset represents a **multi-class image classification** problem because:

- Each image belongs to one class only.
- The goal is to predict a single label for an image.
- No bounding boxes or segmentation masks are provided.

Classes:
- normal
- scratch
- dent
- stain


# Dataset Description

Dataset folders:

```text
images/
│
├── normal/
├── scratch/
├── dent/
└── stain/
```

## Class Descriptions

| Class | Description |
|---|---|
| normal | Product surface without defects |
| scratch | Surface with scratch marks |
| dent | Surface with dent-like marks |
| stain | Surface with stain-like marks |


# Project Structure

```text
part-2-cnn-computer-vision/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
│
├── results/
│   ├── accuracy_loss_curves.png
│   ├── confusion_matrix.png
│   ├── class_distribution.png
│   └── sample_images.png
│
└── sample_predictions/
    └── prediction_outputs.png
```


# Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn


# Task 1: Problem Identification

The dataset is suitable for **Image Classification** because each image contains only one target label.

The CNN model predicts one of the following:
- normal
- scratch
- dent
- stain


# Task 2: Dataset Exploration

Dataset exploration includes:

- Number of classes
- Number of images per class
- Sample images
- Image dimensions
- Dataset imbalance analysis

Generated outputs:
- `class_distribution.png`
- `sample_images.png`


# Task 3: Image Preprocessing

The following preprocessing steps were applied:

## 1. Image Resizing

All images were resized to:

```python
128 × 128
```

## 2. Normalization

Pixel values were normalized:

```python
0–255 → 0–1
```

## 3. Train-Test Split

Dataset split:
- 80% Training
- 20% Testing

## 4. Data Augmentation

Applied augmentations:
- Rotation
- Zoom
- Horizontal Flip

Purpose:
- Reduce overfitting
- Improve generalization


# Task 4: CNN Model Architecture

The CNN model contains:

- Convolution Layers
- ReLU Activation
- Max Pooling Layers
- Flatten Layer
- Dense Layers
- Softmax Output Layer

## CNN Architecture Summary

```text
Input Layer
↓
Conv2D + ReLU
↓
MaxPooling
↓
Conv2D + ReLU
↓
MaxPooling
↓
Conv2D + ReLU
↓
MaxPooling
↓
Flatten
↓
Dense Layer
↓
Dropout
↓
Output Layer (Softmax)
```


# Task 5: Model Training and Evaluation

## Evaluation Metrics

The model evaluation includes:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss
- Test Accuracy
- Confusion Matrix
- Classification Report

Generated outputs:
- `accuracy_loss_curves.png`
- `confusion_matrix.png`
- `prediction_outputs.png`


# Task 6: CNN Concept Explanation

## What is Convolution?

Convolution is a mathematical operation where filters scan across an image to detect important features such as:
- edges
- textures
- shapes

CNNs automatically learn these filters during training.


## Why is Pooling Used?

Pooling reduces the spatial size of feature maps.

Benefits:
- Reduces computation
- Prevents overfitting
- Improves efficiency

Max pooling keeps the strongest feature values.


## Why is ReLU Commonly Used?

ReLU (Rectified Linear Unit):

```python
f(x) = max(0, x)
```

Benefits:
- Faster training
- Adds non-linearity
- Prevents vanishing gradients


## Why CNNs Are Better Than Feed-Forward Networks for Images

CNNs:
- Preserve spatial information
- Learn local image patterns
- Require fewer parameters
- Automatically extract features

Feed-forward networks flatten images and lose spatial relationships.


# Task 7: Business Use Case Mapping

## Manufacturing Quality Inspection

This solution can be used in manufacturing industries to automatically inspect products for defects.

### Real-World Applications

- Automobile manufacturing
- Electronics inspection
- Metal surface inspection
- Packaging quality control

### Benefits

- Faster inspection
- Reduced human error
- Lower operational costs
- Improved product quality
- Real-time defect detection

### Workflow

1. Product image captured using camera
2. CNN analyzes image
3. Defect type predicted
4. Defective products removed automatically


# Model Results

The trained CNN model successfully learns visual defect patterns and classifies images into:
- normal
- scratch
- dent
- stain

Outputs generated:
- Accuracy/Loss Curves
- Confusion Matrix
- Sample Predictions


# Installation Instructions

## Clone Repository

```bash
git clone <repository-link>
```


## Install Dependencies

```bash
pip install -r requirements.txt
```


# Run the Notebook

```bash
jupyter notebook
```

Open:

```text
notebook.ipynb
```

Run all cells sequentially.


# Requirements

Main libraries used:

```text
tensorflow
keras
numpy
pandas
matplotlib
seaborn
opencv-python
scikit-learn
Pillow
jupyter
```


# Future Improvements

Possible enhancements:

- Transfer Learning (ResNet, EfficientNet, MobileNet)
- Real-time camera integration
- Industrial deployment
- Larger datasets
- Hyperparameter tuning
- Defect localization


# Conclusion

This project demonstrates how CNNs can automate manufacturing defect detection using image classification techniques.

The CNN successfully learns visual features such as:
- scratches
- dents
- stains

This forms the foundation for real-world AI-powered industrial inspection systems.
Course: Computer Vision with CNNs

Project: Manufacturing Defect Detection Using CNN
