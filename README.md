# Breast Cancer Histopathology Classification 🎗️

## Project Overview
This project implements a complete Computer Vision pipeline for classifying breast cancer histopathology images (Benign vs. Malignant) using the **BreakHis Dataset**. The project focuses on maximizing diagnostic accuracy using Deep Learning (**DenseNet121**), outperforming standard lightweight models.

It covers the four standard phases of a CV system:
1.  **Acquisition:** Handling high-resolution medical images (400X magnification).
2.  **Enhancement:** Preprocessing and Data Augmentation.
3.  **Segmentation:** Region of Interest (ROI) isolation using Otsu's Thresholding.
4.  **Recognition:** Classification using Transfer Learning with DenseNet121.

## 📊 Results vs. Reference Paper
This project references the paper *"AdaptoVision (2025)"*. While the paper focused on efficiency, this project prioritized medical accuracy.

| Model | Accuracy | Focus |
| :--- | :--- | :--- |
| Reference Paper (AdaptoVision) | ~95.3% | Efficiency (Mobile) |
| **My Proposed Model (DenseNet121)** | **96.7%** | **High Accuracy (Medical)** |

## 🛠️ Phases & Methodology

### 1. Image Acquisition
Used the **BreakHis** dataset, filtering specifically for **400X magnification** images to capture fine tissue details.

### 2. Enhancement
Applied data augmentation techniques including:
* Rescaling (Normalization)
* Rotation, Zoom, and Flips
* **Goal:** To prevent overfitting and generalize the model to new tissue samples.

### 3. Segmentation
Demonstrated tissue isolation using **Otsu's Thresholding** to separate the specimen from the background.

### 4. Recognition (The Model)
* **Architecture:** DenseNet121 (Pre-trained on ImageNet).
* **Technique:** Fine-Tuning (Unfreezing weights) with a low learning rate (`1e-5`).
* **Optimizer:** Adam.
* **Loss Function:** Binary Crossentropy.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/YourUsername/Breast-Cancer-Histopathology-Classification.git](https://github.com/YourUsername/Breast-Cancer-Histopathology-Classification.git)
