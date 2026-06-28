# Brain Tumor AI Diagnosis System
Autonomous Computer Vision Pipeline via ResNet50 Backbone

## Project Overview
This repository contains the source code for an autonomous medical image classification system designed to analyze brain MRI scans. The primary focus of this research is to classify scans into three distinct types of brain tumors (Glioma, Meningioma, Pituitary) alongside Normal tissues (No Tumor), while resolving the visual boundary confusion between Glioma and Meningioma scans.

## Methodology
The pipeline is built using the PyTorch framework and leverages Transfer Learning via a ResNet50 Backbone with custom architectural enhancements:
1. Custom Multi-Layer Feature Classifier: Added a dense neural layer structure to isolate subtle grayscale intensity patterns in MRI scans.
2. Cost-Sensitive Loss Function: Deployed class-weight parameters within the loss function to penalize misclassifications during backpropagation.
3. Stable Optimization: Controlled the learning rate decay dynamically using a learning rate scheduler to lock the model into its optimal weights.

## Evaluation Results
Tested rigorously on a validation dataset of 1,600 unseen clinical MRI images, the finalized weights achieved:
* Overall Validation Accuracy: 95%
* Glioma Precision: 1.00 (Zero false-positive diagnostics)
* Meningioma Recall: 0.99 (Flawless diagnostic sensitivity)
* Normal Tissue Protection: 0.99 Recall (Ensuring diagnostic patient safety)

## Live System Interface
The trained model weights are deployed into a live interactive production environment. You can upload an MRI scan and see the model analyze it in real-time here:

🌐 Live AI Platform: https://huggingface.co/spaces/Isra-Bouchentouf/Brain-Tumor-AI-Diagnosis
