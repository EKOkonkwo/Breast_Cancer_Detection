# Breast_Cancer_Detection
Deep learning pipeline for mammogram classification using ResNet50, VGG16, and a Hybrid ResNet–Vision Transformer (ViT).

# Dataset
CBIS-DDSM dataset with 6,788 ROI images (masses + calcifications).
Binary labels: Malignant = 1, Benign = 0.
Images resized to 224x224, converted to RGB, standardized.

# Methods
Transfer learning using ImageNet pretrained models.
Fine-tuning top layers for domain adaptation.
Hybrid ResNet–ViT for combined local + global feature extraction.
Data augmentation: flips, brightness, contrast, saturation, oversampling.

# Features
Full preprocessing + augmentation pipeline.
Training scripts for all three architectures.
Explainability with Grad-CAM (CNN) and ViT attention maps.
Supports balanced dataset loading and standardized model training.

# Results (Summary)
ResNet50: 98.08% accuracy, 0.9992 AUC.
VGG16: 97.60% accuracy, 0.9940 AUC.
Hybrid ResNet–ViT: 96.79% accuracy, 0.9925 AUC.

# Model Summary
Model               | Acc     | AUC     | Precision | Recall | F1     | Loss
ResNet50-CNN        | 98.08%  | 0.9992  | 0.9760    | 0.9765 | 0.9762 | 0.0852
VGG16-CNN           | 97.60%  | 0.9940  | 0.9752    | 0.9772 | 0.9761 | 0.0970
Hybrid ResNet–ViT   | 96.79%  | 0.9925  | 0.9600    | 0.9647 | 0.9623 | 0.1039

# Objective
Build an accurate, interpretable, and scalable breast cancer detection system using deep learning and hybrid attention mechanisms.
