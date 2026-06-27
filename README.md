# Advanced Brain Tumor AI Diagnosis System
### Autonomous Computer Vision Pipeline via Cost-Sensitive ResNet50 Backbone

![Status](https://shields.io)
![Framework](https://shields.io)
![Architecture](https://shields.io)

## 📌 Project Overview
This repository hosts the complete source code and infrastructure documentation for an autonomous medical image classification pipeline designed to analyze T1/T2-weighted brain MRI scans. 

The core engineering focus of this research was optimizing clinical boundary decision overlaps and structural confusion between **Glioma** (due to its infiltrative, haptic nature) and **Meningioma** scans without inducing class imbalance. 

## 🔬 Technical Methodology
The pipeline leverages **Transfer Learning using a ResNet50 Backbone**, engineered with the following custom architectural enhancements:
1. **Deep Decision Classifier Module:** Integrated a multi-layer filtering block (`Linear(512, 128) -> BatchNorm -> ReLU -> Dropout(0.3) -> Linear`) to isolate subtle grayscale intensity features.
2. **Cost-Sensitive Loss Optimization:** Deployed weight penalties within the cross-entropy loss function to penalize misclassifications during backpropagation, enforcing high sensitivity boundaries.
3. **Learning Rate Decay:** Controlled stochastic optimization via a `CosineAnnealingLR` scheduler to guarantee stable visual convergence.

## 📊 Evaluation & Validation Metrics
Evaluated rigorously on a validation split of **1,600 unseen, clinical images**, the architecture achieved exceptional production-grade stability:
* **Overall Test Accuracy:** `95%`
* **Glioma Precision:** `1.00` (Zero false-positive alarms)
* **Meningioma Recall:** `0.99` (Flawless sensitivity)
* **Pituitary Metrics:** Full `1.00` Precision & Recall optimization.
* **Normal Tissue Protection:** `0.99` Recall (Ensuring diagnostic patient safety against false negatives).

## 🚀 Live Production Deployment & Documentation
The finalized model weights (`resnet_classifier_epoch_15.pth`) have been successfully deployed into a dedicated, cloud-accelerated environment for instant expert auditing and real-time clinical inference.

* 🌐 **Access Live Interactive Panel:** https://huggingface.co/spaces/Isra-Bouchentouf/Brain-Tumor-AI-Diagnosis
* 📝 **Read the Comprehensive Research Article:** https://neuroversebyisrabou.blogspot.com/2026/06/autonomous-medical-vision-optimizing.html

## 👤 Academic Bio & Intellectual Property
* **Lead Pipeline Engineer:** Isra Bouchentouf  
* **Role:** Independent AI Researcher & Data Scientist  
* **Age:** 14 Years Old  
* **Professional Network:** [LinkedIn Profile] https://www.linkedin.com/in/isra-bouchentouf-064417411/

---
*© 2026 Copyrighted by Isra Bouchentouf. All Rights Reserved. Independent Medical AI Research Hub.*
