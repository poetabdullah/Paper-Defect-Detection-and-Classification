# Paper Defect Detection and Classification

## Overview

This project focuses on automating defect localization in industrial quality control using advanced feature extraction and machine learning techniques. It explores methods such as Histogram of Oriented Gradients (HOG), Gabor filters, Canny edge detection, and Wavelet Transform combined with Support Vector Machines (SVMs), Convolutional Neural Networks (CNNs), and ensemble learning to enhance defect detection accuracy.

## Articles
If you want to have a detailed understanding of this project, you can refer to to the following articles on **Medium**:
- **Defect Detection in Papers & Model Comparison**: https://medium.com/@abdullahimranarshad/defect-detection-in-papers-model-comparison-a0a44a4bafa6
  
- **Feature Extraction and Data Preprocessing in Computer Vision**: https://medium.com/@abdullahimranarshad/feature-extraction-and-data-preprocessing-in-computer-vision-53066a812a96

## Workflow Summary

### Data Exploration

- **Loading Images:** Loaded and verified image data.
- **Class Distribution:** Checked and balanced class distributions.
- **Data Preprocessing:** Preprocessed images for analysis.

### Feature Extraction

- **Color Format Check:** Verified image color formats.
- **Color Histogram:** Analyzed but did not yield significant results.
- **Spatial Binning:** Analyzed overall image features, not specific to defects.
- **Histogram of Oriented Gradients (HOG):** Effective in capturing defect features.
- **Local Binary Patterns:** Limited effectiveness due to image blurring.
- **Gabor Filters:** Effective in identifying minor defects.
- **Canny Edge Detection:** Highly effective in defect edge detection.
- **Wavelet Transform:** Provided insights across different resolutions.

### Dimensionality Reduction

- **Feature Set:** Built using HOG, Gabor filters, Canny edge detection, and wavelet transform.
- **PCA Application:** Reduced dimensionality while maintaining 90% variance.

### Model Building

- **Logistic Regression:** Achieved 99% train and 79% test accuracy after optimization.
- **Gaussian Naive Bayes:** Similar accuracy improvements after optimization.
- **Support Vector Machines (SVMs):** Achieved 86% train and 80% test accuracy without additional tuning.
- **Convolutional Neural Networks (CNNs):** Despite efforts, achieved only 38% test accuracy, indicating need for improvement.
- **Combined Models:** Achieved 90% train and 81% test accuracy by combining SVM, logistic regression, and Naive Bayes.

### Defect Localization

- **Visualization:** Used trained models to visualize defects on paper samples.

### Important Notes

- **Code Inclusion:** Includes only crucial and optimized code sections.
- **Omitted Code:** Excludes less effective or redundant code sections.
- **Improvement Potential:** Suggestions for further model fine-tuning and CNN optimization.
- **Data Visualization:** Extensive but omitted for brevity.


Feel free to provide your valuable insights into improving this project.
