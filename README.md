# CowCoders – Skin Cancer Detection Model

## Problem Statement  
Dermatological screening and histopathology remain the standard for diagnosing skin cancer, but they suffer from delays (appointments, lab processing) and variability (expertise, image quality). The goal of this system is to provide a faster, scalable method for identifying suspicious lesions—potentially reducing screening time and enabling earlier intervention.

## Motivation  
With the growing incidence of skin cancer and limited access to dermatological services in many regions, an automated detection tool can help diagnose skin cancer early on. The motivation is to harness advances in convolutional neural networks (CNNs) and transfer learning to improve accessibility and accuracy of skin-lesion classification.

## Dataset  
This project uses the HAM10000 dataset, available on Kaggle:  
https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000  

The dataset contains **10,015 dermatoscopic images** of pigmented skin lesions collected from different populations and acquired using various types of dermatoscopic equipment.  
It includes **both benign and malignant lesion classes**, allowing for effective training of deep learning classifiers.


## Methodology  
### Pre-processing*
- Images are resized, normalized (pixel values scaled, e.g., from `[0,255]` → `[0,1]`).  
- Data augmentation (flips, rotations, zoom) applied to enhance training variety and mitigate class imbalance.

### Model Architecture*
- A convolutional neural network is used (specify your architecture).  
- Layers include: convolutional blocks, pooling, dropout for regularisation, flatten and dense layers for classification.  
- The final layer uses softmax (for multi-class) or sigmoid (for binary) classification.

### Training & Evaluation  
- Loss function: e.g., binary cross-entropy (or categorical cross-entropy).  
- Optimiser: e.g., Adam with learning rate 0.0001, momentum, etc.  
- Training epochs: [insert number]; batch size: [insert number].  
- Metrics: Accuracy, Recall (Sensitivity), Precision, F1-Score, AUC (if applicable).  
- Model validated on hold-out test set; confusion matrix and classification report generated.

## Results  
- Best obtained accuracy: [insert %]  
- Sensitivity (Recall) for malignant class: [insert %]  
- Precision for malignant class: [insert %]  
- F1-Score: [insert value]  
- (Optional) AUC: [insert value]

