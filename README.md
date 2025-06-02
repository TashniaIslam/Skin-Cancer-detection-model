# Skin-Cancer-detection-model
## Project Overview

Skin cancer affects millions globally, and early detection is crucial. However, access to dermatologists and diagnostic equipment is often limited in remote or under-resourced areas. Our solution leverages deep learning and **knowledge distillation** to create a lightweight model suitable for mobile and web deployment.

We used high-performance models (ResNet50, DenseNet169) as teachers and distilled their knowledge into a compact **MobileNetV2** student model to enable fast, accurate classification of skin lesion images from the **HAM10000 dataset**.

## Objectives

- Train high-accuracy teacher models (ResNet50 & DenseNet169).
- Use knowledge distillation to train a compact MobileNetV2 student model.
- Improve classification robustness using ensemble learning.
- Deploy a web-based system for real-time skin cancer detection.

## Methodology

- **Dataset**: HAM10000 (10,015 dermatoscopic images, 7 classes).
- **Data Augmentation**: Rotation, flipping, brightness adjustment, zooming, etc.
- **Model Training**:
  - Teachers: ResNet50, DenseNet169 (transfer learning).
  - Student: MobileNetV2 with KD (α = 0.8, T = 50).
- **Loss Function**: Hybrid of KL Divergence and Cross-Entropy.
- **Frameworks**: TensorFlow, Keras, OpenCV, Flask.

## Results

| Model         | Accuracy | Parameters | Inference Time |
|---------------|----------|------------|----------------|
| ResNet50      | 67.86%   | 94.77 MB   | 631 ms/batch   |
| DenseNet169   | 87.76%   | 51.88 MB   | 631 ms/batch   |
| MobileNetV2   | 66.94%   | 34.65 MB   | 517 ms/batch   |

## Features
✅ Knowledge Distillation implementation from ResNet50 & DenseNet169 to MobileNetV2

✅ Custom training loop using TensorFlow

✅ Augmented training with brightness, flipping, shifting, zoom, etc.

✅ Stratified train-validation-test split

✅ Model saving and evaluation with accuracy and confusion matrix

## Future Enhancements
Use GANs or SMOTE to balance underrepresented classes

Add Grad-CAM visualizations for interpretability

Port the student model to TensorFlow Lite for mobile deployment

Improve accuracy using MobileNetV3 or EfficientNet as student models

## License
This project is submitted as part of the EEE 4709 course and is intended for academic use only.

## Disclaimer
This is an ongoing project work. Currently, we are working to reduce the data imbalance and make the model more accurate. Therefore, this is not the final code and the final model. 
