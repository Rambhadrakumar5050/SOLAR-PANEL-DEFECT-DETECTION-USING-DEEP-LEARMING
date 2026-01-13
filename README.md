# Solar Panel Defect Detection Using Deep Learning

This repository contains the implementation of our academic project **“Solar Panel Defect Detection Using Deep Learning”**, developed as part of the CSE curriculum at **IIIT Vadodara**.

The project uses **Convolutional Neural Networks (CNNs)** and **transfer learning** to detect and classify defects in solar panel images.

---

## 👨‍🎓 Authors
- Badabagni Rohini (202311019)
- Chintha Punyamurthy (202311023)
- Chitikela Rambhadra Kumar (202311024)

**Under the guidance of:**  
Dr. B. Venkata Phani Krishna  
Department of CSE, IIIT Vadodara

---

## 📌 Project Overview

Manual inspection of solar panels is time-consuming and error-prone.  
This project proposes a **deep learning–based automated fault detection system** capable of identifying multiple solar panel surface conditions.

### Defects Covered:
- Clean
- Dusty
- Snow-covered
- Bird-drop
- Physical damage
- Electrical damage

---

## 📊 Dataset

- Source: Kaggle – Solar Panel Images (Clean and Faulty)
- Total images: **869**
- Image size: **224 × 224**
- Augmentation techniques:
  - Rotation
  - Horizontal flip
  - Brightness adjustment

---

## 🧠 Models Used (Transfer Learning)

- VGG16
- ResNet50
- InceptionV3
- MobileNetV2
- EfficientNetB0

Pre-trained ImageNet weights were used, and custom classification heads were added.

---

## 🔍 Classification Stages

### 1️⃣ Binary Classification
**Defective vs Non-Defective**

- Non-defective class split into balanced batches
- Same damaged images (172) used with different non-damaged batches
- Train / Validation / Test split: **70% / 20% / 10%**

---

### 2️⃣ Defective Classification
**Electrical Damage vs Physical Damage**

- Augmented to balance classes
- Train / Validation / Test split: **70% / 15% / 15%**

---

### 3️⃣ Non-Defective Classification
**Clean vs Non-Clean (Dust, Snow, Bird-drop)**

- Batch-wise balanced training
- Train / Validation / Test split: **70% / 15% / 15%**

---

### 4️⃣ Multi-Class Classification
- Non-clean: Dust vs Snow vs Bird-drop
- Six-class classification for all defects

---

## 🤝 Ensemble Learning

Predictions from multiple CNN models were averaged to improve accuracy.  
Ensemble models consistently outperformed individual models.

---

## 📁 Repository Structure

