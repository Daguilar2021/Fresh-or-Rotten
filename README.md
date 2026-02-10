# 🍎 Fresh vs Rotten Fruit Classification using CNNs

## 📌 Project Overview
This project implements a **Convolutional Neural Network (CNN)** to classify images of fruit as **Fresh** or **Rotten** using deep learning techniques. The model is trained on a limited dataset and focuses on mitigating overfitting through **data augmentation, regularization, and early stopping**.

The project demonstrates an end-to-end machine learning workflow, including dataset preprocessing, model design, evaluation, and performance analysis.

---

## 🧠 Motivation
Food waste is a global issue, and automated image-based quality inspection systems can help reduce unnecessary waste. This project serves as a **proof-of-concept** for image classification systems that could later be extended to smart inventory or agricultural monitoring applications.

---

## 🗂️ Dataset
- Binary classification: **Fresh (0)** vs **Rotten (1)**
- Image resolution: **150 × 150 × 3**
- Dataset size: ~5,000+ images
- Dataset **not included** in this repository due to size constraints

---

## 🏗️ Model Architecture
model is a sequential CNN composed of 3 convolutional Blocks

### Convolutional Blocks
- **3 Convolutional Blocks**, each containing:
  - `Conv2D` + ReLU activation  
  - `MaxPooling`  
  - `Dropout`

### Fully Connected Layers
- `Dense` layer with **512 units** and ReLU activation  
- `Dropout`

### Output Layer
- `Dense` layer with **Sigmoid activation** for binary classification 

---

## ⚙️ Training Configuration
- **Optimizer:** Adam  
- **Loss Function:** Binary Crossentropy  
- **Metric:** Accuracy  
- **Batch Size:** 32  
- **Epochs:** 5 *(with early stopping)*  

---

## 🔄 Data Augmentation
To improve generalization on a small dataset, the following augmentation techniques were applied during training:

- Rotation  
- Width and height shifting  
- Shearing  
- Zooming  
- Horizontal and vertical flipping  
- Reflect padding  

---

## 📊 Results
### Best Baseline Performance
The following results correspond to the **best-performing baseline model** trained over 5 epochs with data augmentation and early stopping enabled.

- **Training Accuracy:** ~91.6%  
- **Validation Accuracy:** **~88.3%**  
- **Training Loss:** ~0.21  
- **Validation Loss:** **~0.26**  

### Training Observations
- The model shows **steady improvement** in both training and validation accuracy across epochs.
- Validation loss decreases consistently and reaches its lowest value at **Epoch 5**, indicating **good generalization**.
