
# 🧠 Brain Tumor Detection Project

This project detects brain tumors from MRI scans using a hybrid approach of classical image segmentation and deep learning classification. High-intensity tumor regions are extracted, resized, and classified using pre-trained CNN models (like VGG19 and EfficientNet) to achieve high accuracy.

## 🔍 Project Overview

- **Dataset**: MRI brain scan images, classified into glioma, meningioma, pituitary, and no tumor categories.
- **Segmentation**: Classical image processing techniques (CLAHE, thresholding, contour-based region detection) to isolate tumor regions.
- **Classification**: Transfer learning using VGG19 and EfficientNetB0 to classify cropped tumor regions.
- **Goal**: Improve detection accuracy beyond 71.5% by focusing only on high-intensity tumor regions.



## 📊 Train-Test Split

- **Train/Validation/Test**: 70% training, 20% validation, 10% testing.
- Stratified splits used to maintain class balance across sets.

## ✅ Performance Metrics

- **Metrics used**:
  - Precision
  - Recall
  - F1 Score
  - Accuracy
- These help in understanding the model performance beyond simple accuracy.

## ⚙️ Hyperparameters

- Optimizer: Adam
- Learning Rate: 0.0001
- Epochs: 15
- Batch Size: 32
- Data Augmentation: Rescale, Rotation, Zoom, Shear

## 🖼️ Image Preprocessing

- All images resized to 64x64 or 224x224 (depending on model input requirement).
- CLAHE used to enhance contrast before segmentation.
- Only high-intensity contours >500px area are considered for cropping.

## 📌 Key Libraries Used

- OpenCV
- TensorFlow / Keras
- NumPy, Matplotlib
- Scikit-learn

## 🧪 Results

- Achieved up to **91% accuracy** with EfficientNetB0 on segmented tumor data.
- Improved detection on ambiguous cases through preprocessing.

---

**Authors**: Vignesh et al.  
**License**: MIT
