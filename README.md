# Multimodal Phishing Website Detection using Deep Learning

## Overview

Phishing websites pose a significant threat by deceiving users into revealing sensitive information through malicious URLs and fake webpage designs.

This project proposes a **multimodal deep learning approach** that combines both:

* URL-based features (textual patterns)
* Screenshot-based features (visual appearance)

to improve phishing detection performance.

---

## Objective

* Detect phishing websites more accurately by leveraging multiple data modalities
* Improve robustness compared to single-modality models

---

## Methodology

### 1. Data Collection

* Phishing URLs: PhishTank
* Legitimate URLs: Tranco
* Webpage screenshots captured using automated tools

---

### 2. Data Preprocessing

* URL cleaning and tokenization
* Image resizing and normalization

---

### 3. Model Architecture

#### URL Models

* GRU
* BiGRU
* BiLSTM
* 1D-CNN
* Hybrid BiLSTM-BiGRU

#### Image Model

* DenseNet121 (pretrained)

---

### 4. Feature Extraction & Fusion

* Each model is trained independently
* Final classification layers are removed
* Intermediate features are extracted as embeddings
* Features from URL and image are combined (**feature-level fusion**)
* Fully connected layer used for final classification

---

### 5. Training & Evaluation

* Loss: Binary Crossentropy
* Metrics: Accuracy, Precision, Recall, F1-score
* Early stopping and hyperparameter tuning applied

---

## Results

* Multimodal model outperformed single-modality models
* Best performance achieved using:

  * **BiGRU (URL) + DenseNet121 (Image)**
* Improved generalization and robustness

---

## Key Contributions

* Proposed multimodal framework combining URL and image features
* Implemented feature-level fusion approach

---

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* Pandas, NumPy
* Scikit-learn

---

## Author

Lau Jia Qi
Final Year Computer Science (Data Science) Student
Multimedia University

---
