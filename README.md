# 🧠 Brain Tumor Detection using Deep Learning

This project focuses on detecting brain tumors from MRI images using deep learning techniques. It leverages transfer learning with a pretrained Convolutional Neural Network (CNN) to classify MRI scans into tumor and non-tumor categories.

---

## 📌 Overview

Brain tumors are life-threatening conditions that require early and accurate diagnosis. Manual analysis of MRI scans can be time-consuming and subjective. This project aims to assist in automated diagnosis by building a deep learning model that can classify MRI images with high accuracy.

---

## 🗂️ Dataset

- The dataset consists of labeled MRI images of brain scans.
- Images are organized into class-based directories (e.g., tumor vs non-tumor or multiple tumor types).
- Data is loaded dynamically from directory paths for scalability.

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Images are resized to a fixed input size compatible with the model.
- Normalization is applied to scale pixel values.
- Data is shuffled to remove ordering bias.
- Batch-wise loading is implemented using generators for memory efficiency.

### 2. Model Architecture
- Transfer learning using **VGG16** pretrained on ImageNet.
- Base model layers are frozen initially.
- Custom classification head added:
  - Fully connected (Dense) layers
  - Dropout layers for regularization
  - Softmax output layer for classification

### 3. Training
- Loss Function: Sparse Categorical Crossentropy
- Optimizer: Adam (low learning rate for fine-tuning)
- Metrics: Accuracy
- Model trained over multiple epochs with validation tracking

### 4. Evaluation
- Model performance evaluated using:
  - Accuracy curves (training vs validation)
  - Confusion matrix
  - Classification report (precision, recall, F1-score)

---

## 🚀 Results

- The model successfully learns discriminative features from MRI images.
- Transfer learning significantly improves performance even with limited data.
- Achieves strong classification accuracy for tumor detection tasks.

---

## 🧩 Pipeline Design

The project follows a modular pipeline:

1. Data Loading  
2. Preprocessing & Augmentation  
3. Model Building (Transfer Learning)  
4. Training & Validation  
5. Evaluation & Visualization  

This design ensures:
- Reproducibility  
- Easy experimentation  
- Scalability for larger datasets  

---

## 💡 Key Insights

- Transfer learning is highly effective for medical imaging tasks with limited data.
- CNNs can capture subtle spatial patterns relevant to tumor detection.
- Automated systems like this can support radiologists in early diagnosis.

---

## 🛠️ Tech Stack

- Python  
- TensorFlow / Keras  
- NumPy  
- PIL (Image Processing)  
- Scikit-learn  


