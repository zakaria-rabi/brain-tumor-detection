# 🧠 Brain Tumor Detection with Deep Learning

> CNN-based medical image classification for brain tumor detection

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)](https://keras.io)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)](https://kaggle.com)

---

## 🎯 Overview

Deep learning project for **automatic brain tumor detection** from MRI images using a **Convolutional Neural Network (CNN)**. The model classifies MRI scans into two categories: **tumor** and **no tumor**.

This project demonstrates the application of Computer Vision and Deep Learning in the medical imaging domain.

---

## 🏗️ Architecture

```
Input (MRI Image)
       ↓
Conv2D + ReLU + MaxPooling
       ↓
Conv2D + ReLU + MaxPooling
       ↓
Conv2D + ReLU + MaxPooling
       ↓
Flatten
       ↓
Dense (fully connected)
       ↓
Dropout (regularization)
       ↓
Output: Tumor / No Tumor (Sigmoid)
```

---

## 📁 Structure

```
brain-tumor-detection/
│
├── data/
│   ├── yes/                  # MRI images with tumor
│   └── no/                   # MRI images without tumor
│
├── notebooks/
│   ├── preprocessing.ipynb   # Data loading & augmentation
│   ├── training.ipynb        # Model training
│   └── evaluation.ipynb      # Results & visualization
│
├── model/
│   └── brain_tumor_cnn.h5    # Saved trained model
│
├── src/
│   ├── preprocess.py         # Image preprocessing functions
│   ├── model.py              # CNN architecture definition
│   └── predict.py            # Inference on new images
│
└── requirements.txt
```

---

## 📊 Dataset

- **Source:** [Kaggle — Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)
- **Classes:** Tumor (`yes`) / No Tumor (`no`)
- **Preprocessing:** Resize → Normalize → Augmentation (flip, rotation, zoom)

---

## 📈 Results

| Metric | Score |
|--------|-------|
| Accuracy | ~90%+ |
| Loss | Low (converged) |
| Validation Accuracy | ~88%+ |

---

## 🛠️ Setup

```bash
git clone https://github.com/zakaria-rabi/brain-tumor-detection.git
cd brain-tumor-detection
pip install -r requirements.txt
```

**Requirements:**
```
tensorflow
keras
numpy
pandas
matplotlib
scikit-learn
opencv-python
jupyter
```

---

## 🚀 Usage

```python
from src.predict import predict_tumor

# Predict on a new MRI image
result = predict_tumor("path/to/mri_image.jpg")
print(result)  # Output: "Tumor Detected" or "No Tumor Detected"
```

---

## 🌍 Applications

- Early detection of brain tumors from MRI scans
- Assisting radiologists in diagnosis
- Healthcare AI automation

---

## 👤 Author

**Zakaria Rabi** — Master IARO, Moulay Ismail University  
📧 zakariarabi662@gmail.com | 🐙 [github.com/zakaria-rabi](https://github.com/zakaria-rabi)
