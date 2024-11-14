# ResUNet-Steel: Enhancing Steel Defect Detection with Residual Networks and U-Net Architecture

## Overview
ResUNet-Steel is a deep learning-based system designed to automate defect detection in steel manufacturing. By integrating ResNet classification with U-Net segmentation, this model offers both high-level defect identification and precise localization, enabling manufacturers to improve quality control, reduce waste, and enhance production efficiency.

## Table of Contents
- [Project Objectives](#project-objectives)
- [Data Collection](#data-collection)
- [Model Architecture](#model-architecture)
  - [ResNet Classifier](#resnet-classifier)
  - [ResUNet Segmentation Model](#resunet-segmentation-model)
- [Implementation](#implementation)
- [Results](#results)
- [Future Work](#future-work)
- [References](#references)

## Project Objectives
1. **Enhanced Quality Control:** Automate early defect detection to ensure manufacturing quality.
2. **Reduced Waste:** Minimize faulty products, thus reducing scrap and associated costs.
3. **Real-time Detection:** Enable immediate response to detected defects, increasing production efficiency.

## Data Collection
The dataset contains 12,600 high-resolution images of steel surfaces labeled for four types of defects. These images reflect diverse manufacturing conditions to ensure the model’s robustness. Pixel-level annotations allow for precise segmentation of defect regions.

## Model Architecture
### ResNet Classifier
The ResNet-based classifier is used to detect whether a defect is present. It employs residual blocks to avoid vanishing gradient issues, enabling the model to learn complex features even with increased depth.

### ResUNet Segmentation Model
ResUNet combines ResNet's feature extraction with U-Net's encoder-decoder structure for pixel-level defect localization. Skip connections retain critical spatial information, allowing precise segmentation of defect boundaries.

## Implementation
1. **Preprocessing and Augmentation:** Data preprocessing and augmentation, including rotations and flips, enhance generalization.
2. **Training:** The model is trained using pixel-wise loss for accurate segmentation, with optimizations like batch normalization for real-time performance.
3. **Data Compression:** Run-Length Encoding (RLE) compresses segmentation masks, reducing memory usage while retaining spatial information.

## Results
The ResUNet model achieves high accuracy, measured with metrics like IoU, Precision, Recall, and F1-score. The model demonstrates robustness in defect detection across various conditions, making it suitable for industrial applications.

## Future Work
- Extend the model to handle larger datasets and diverse defect types.
- Integrate additional advanced techniques, such as hybrid learning strategies, to improve performance and expand applicability across materials and industries.

## References
Refer to the project documentation for a comprehensive list of related research and resources that informed this project.
