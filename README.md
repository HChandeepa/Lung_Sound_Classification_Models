# PulmoSense AI: Lung Sound Classification using Deep Learning

PulmoSense AI is a comprehensive lung sound classification system designed to identify respiratory conditions (e.g., wheeze, crackle) through deep learning techniques applied to audio signals. This project includes data preprocessing, augmentation, feature extraction, and model development—culminating in a robust classification pipeline with ensemble learning and inference support.

## 🌐 Project Overview

Respiratory sound analysis is crucial for early detection of pulmonary diseases. This system leverages modern deep learning and audio signal processing to build an end-to-end classification model trained on curated and preprocessed lung sound data.

---

## 🧠 Model Architecture

Three deep learning models were developed and trained:

### 1. **Binary CNN**
- **Purpose**: Classifies whether the lung sound is *normal* or *abnormal*
- **Architecture**: Lightweight convolutional layers with ReLU activations and max pooling
- **Use Case**: Acts as the first-phase screening model

### 2. **CNN (Multiclass)**
- **Purpose**: Performs multiclass classification for *wheeze*, *crackle*, *both*, or *normal*
- **Architecture**: Deep CNN with batch normalization and dropout
- **Advantage**: High precision for spatial feature extraction in lung auscultation data

### 3. **CNN-LSTM (Multiclass)**
- **Purpose**: Multiclass classifier that combines CNN feature extraction with LSTM temporal modeling
- **Architecture**: CNN front-end for spectral features + LSTM layers for sequential patterns
- **Advantage**: Captures both spectral and temporal dependencies in lung sounds

### 🔁 Ensemble Learning
- **Strategy**: Final prediction is generated through hard voting across the three models
- **Benefit**: Improves classification robustness, generalization, and reduces overfitting

---

## 📁 Datasets

This project utilizes two public datasets for training and evaluation:

### 📌 ICBHI 2017 Respiratory Sound Database

- **Source**: International Conference on Biomedical and Health Informatics (ICBHI)
- **Access**: [ICBHI Dataset Link](https://bhichallenge.med.auth.gr/ICBHI_2017_Challenge)
- **Description**:
  - 920 recordings from 126 patients
  - Labeled as **normal**, **wheeze**, **crackle**, or **both**
  - Sample rate: 4,000 Hz
  - Includes metadata like age, gender, diagnosis, and auscultation site
- **Use in Project**:
  - Primary training and validation dataset
  - Undergoes preprocessing, segmentation, and augmentation

---

### 📌 FRAIWAN Respiratory Dataset

- **Source**: Dr. Abdulrahman Fraiwan et al.
- **Access**: [FRAIWAN Dataset on Zenodo](https://zenodo.org/record/7705465)
- **Description**:
  - Labeled recordings of **normal**, **wheeze**, **crackle**, and **stridor**
  - High-fidelity recordings from clinical environments
  - Format suitable for direct ingestion into deep learning pipelines
- **Use in Project**:
  - Supplementary training data to increase class diversity and improve generalization

> ⚠️ These datasets are not included in this repository. Please download them from the official sources above and follow any usage licenses or agreements provided.

---

## 🧠 Features

- Audio normalization and segmentation
- Pitch shifting and noise augmentation
- MFCC and spectral feature extraction
- CNN-based classification models
- Ensemble learning using hard voting
- Performance metrics (accuracy, precision, recall, F1-score, ROC)
- Export-ready models for deployment

---

## 🧪 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/HChandeepa/Lung_Sound_Classification_Models

