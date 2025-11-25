# Breast_Cancer_Detection

Deep learning pipeline for mammogram classification using ResNet50, VGG16, and a Hybrid ResNet–Vision Transformer (ViT).

---

## Table of Contents
1. [Objective](#objective)
2. [Dataset](#dataset)
3. [Methods](#methods)
4. [Features](#features)
5. [Libraries Used](#libraries-used)
6. [Results](#results)
7. [Model Summary](#model-summary-key-metrics)
8. [Future Work](#future-work)

---

## Objective

Build an accurate, interpretable, and scalable breast cancer detection system using deep learning and hybrid attention mechanisms.

---

## Dataset

- **Source:** CBIS-DDSM dataset (Regions of Interest — masses + calcifications)  
- **Total images:** 6,788 ROI images  
- **Labels:** Binary — **Malignant = 1**, **Benign = 0**

---

## Methods

- Transfer learning with ImageNet-pretrained backbones (ResNet50, VGG16).  
- Fine-tuning top layers for domain adaptation.  
- **Hybrid ResNet–ViT** to combine local (CNN) and global (Transformer) features.  

---

## Features

- Full preprocessing + augmentation pipeline (configurable).  
- Training scripts for ResNet50, VGG16, and Hybrid ResNet–ViT architectures.  
- Explainability tools:
  - Grad-CAM for CNN backbones.  
  - Transformer attention maps for ViT components.  
- Support for balanced dataset loading and reproducible training.

---

## Libraries Used

- `tensorflow` / `keras` (core model building & training)  
- `torch` / `timm` (optional — alternative ViT implementations)  
- `opencv-python` (image I/O and preprocessing)  
- `numpy`, `pandas` (data handling)  
- `matplotlib`, `seaborn` (visualization)  
- `scikit-learn` (metrics, train/test utilities)  
- `tensorflow-addons` (optional training utilities)

---

## Results

- **ResNet50:** 98.08% accuracy, 0.9992 AUC  
- **VGG16:** 97.60% accuracy, 0.9940 AUC  
- **Hybrid ResNet–ViT:** 96.79% accuracy, 0.9925 AUC

---

## Model Summary (Key metrics)

| Model               | Acc     | AUC     | Precision | Recall | F1     | Loss   |
|---------------------|---------|---------|-----------|--------|--------|--------|
| ResNet50-CNN        | 98.08%  | 0.9992  | 0.9760    | 0.9765 | 0.9762 | 0.0852 |
| VGG16-CNN           | 97.60%  | 0.9940  | 0.9752    | 0.9772 | 0.9761 | 0.0970 |
| Hybrid ResNet–ViT   | 96.79%  | 0.9925  | 0.9600    | 0.9647 | 0.9623 | 0.1039 |

---

## Future Work

- **Expand dataset** using additional public and clinical mammography databases.  
- **Integrate segmentation models** (U-Net, Mask R-CNN) for lesion boundary detection.  
- **Deploy as a cloud-based diagnostic tool** with real-time inference and explainability.  
- **Develop multi-view fusion models** to combine CC and MLO mammogram views.  
- **Add model uncertainty estimation** using Bayesian techniques.  
---
