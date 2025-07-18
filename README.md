# Fake-Currency-Detector
This is  deep learning CNN model which is  used to  classify currency of 500 note into 2 classes real and fake  on custom dataset
# 💰 Fake Currency Detector – 500 INR Note Classification

This repository contains a **PyTorch-based Transfer Learning project** to detect **fake vs real Indian 500 rupee currency notes** using **ResNet18 pretrained on ImageNet**.

---

## 🚀 Project Overview

### 🔍 Objective

To build a robust classifier that predicts whether an uploaded **500 INR note image is fake or real**, leveraging the power of transfer learning and image augmentation techniques.

---

## 🗂️ Dataset
 I have made my own dataset for this project :
 Silent Feature of dataset:
 1. Contain around 997 images of both real and fake note
 2. Sources :- collected from social media , captured by mobile camera
 3. Images are captured with mobile camera with different angles , different background ,different lighting condition and some of them are truncated and occluded
 4. Challenges faced:-  * Dataset has less no. of  mobile captured and web downloading images
                        * small dataset can lead to overfitting and poor learning capacity problem
 6. Solved challenges using Data Augumentation technique  and also use for increasing images in dataset
 6. Dataset has two classes: FAKE 500 AND REAL 500
 7. Transformations Applied:
       - Resize to 224x224
       - Normalization with ImageNet mean and std
 8. Dataset uploaded publicly to kaggle for public for public use and future use
     Dataset Link: [https://www.kaggle.com/datasets/iayushanand/currency-dataset500-inr-note-real-fake ](url)

 9. Use case:
## 🏗️ Model Architecture

- **Base Model:** ResNet18 (pretrained on ImageNet)
- **Modifications:**
  - Final fully connected layer replaced with output for **2 classes** (fake, real)
- **Training Settings:**
  - Loss Function: CrossEntropyLoss
  - Optimizer: Adam
  - Epochs: 30
  - Device: CUDA 

---

## 📈 Training Results

FINAL LOSS :- 0.1036
Accuracy: 0.9719
Test Accuracy: 0.9560

✅ **Model weights saved** as `currency_classifier_resnet18.pth` for deployment and reuse.

---
Kaggle Notebook Link:-https://www.kaggle.com/code/iayushanand/fake-currency-detector/edit/run/251138203 /

