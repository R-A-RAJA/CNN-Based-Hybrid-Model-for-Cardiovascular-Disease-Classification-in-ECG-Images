# 🫀 Optimized CNN-Based Hybrid Model for Multi-Label Classification of Cardiovascular Diseases in 12-Lead ECG Images

## 📘 Overview

This project presents an optimized **Convolutional Neural Network (CNN)-based hybrid model** for the **multi-label classification** of cardiovascular diseases (CVDs) using 12-lead ECG images. The model assists in the accurate, automated interpretation of ECGs by classifying them into the following categories:

- **Normal**
- **Abnormal**
- **Myocardial Infarction (MI)**
- **History of MI**

The system combines the power of **deep learning** for feature extraction with **traditional machine learning classifiers** like **LightGBM** to enhance performance, reduce overfitting, and achieve high accuracy.

---

## 🎯 Objectives

- Develop an end-to-end CNN pipeline to process 12-lead ECG images.
- Extract deep feature representations from ECGs.
- Use LightGBM and other classifiers on these features to improve predictive accuracy.
- Apply data augmentation and class balancing to ensure robustness.

---

## 🧠 Problem Statement

Traditional ECG analysis is manual, time-consuming, and prone to human error. Most deep learning approaches are built for **single-label classification**, but real-world ECGs often contain **multiple co-occurring heart conditions**.

This project aims to build a **robust multi-label classification model** to automate and improve the accuracy of ECG interpretation.

---

## ⚙️ Methodology

### 1. Data Preprocessing

- Resize ECG images to `227×227` pixels.
- Normalize pixel values to `[0,1]`.
- Crop headers/footers to retain only diagnostic regions.
- One-hot encode class labels.
- Apply augmentation techniques:
  - Rotation
  - Shift
  - Zoom
  - Shear

### 2. CNN Model

- Dual-branch architecture:
  - **Stack Branch**: Deep convolutional layers for spatial features.
  - **Full Branch**: Dense layers reshaped and upsampled for high-level features.
- Layers used:
  - `Conv2D`, `MaxPooling2D`, `LeakyReLU`, `BatchNormalization`, `Dropout`, `Flatten`, `Dense`

### 3. Feature Extraction

- Features extracted from the final dense layers of the trained CNN.
- Saved and used as input to machine learning classifiers.

### 4. Classifier Models

- Classifiers trained on CNN-extracted features:
  - ✅ LightGBM (Best performing)
  - XGBoost
  - Random Forest
  - Naïve Bayes etc,.
- Evaluation metrics used:
  - F1-score
  - Precision
  - Recall
  - Confusion Matrix

---

## 🚀 Key Features

- ✅ **Hybrid Approach**: CNN for feature extraction + LightGBM for classification.
- 📈 **Data Augmentation**: Increases dataset diversity and reduces overfitting.
- ⚖️ **Class Imbalance Handling**: Improves prediction fairness.
- 📦 **Scalable Design**: Can scale to larger datasets and more disease classes.
- 🔍 **Model Interpretability**: Feature importance visualized from LightGBM.

---

## 📈 Results

- Achieved up to **99% accuracy** using the **LightGBM classifier**.
- Superior generalization through data augmentation and regularization.
- Training and validation plots show **no signs of overfitting**.

---

