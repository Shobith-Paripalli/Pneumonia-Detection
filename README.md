# Pneumonia Detection Using Deep Learning

## Overview

This project aims to develop a deep learning model for the automated diagnosis of pneumonia from chest X-ray images. Leveraging the power of transfer learning, the VGG19 architecture is employed to achieve high accuracy in classifying X-ray images as either indicative of pneumonia or healthy. This project includes an exploratory data analysis (EDA) phase, model training, validation, and testing, with comprehensive performance metrics to ensure the model's robustness.

## Dataset

The dataset used in this project is sourced from publicly available repositories of chest X-ray images. It is divided into three sets:
- **Training Set**: Used to train the model.
- **Validation Set**: Used to tune hyperparameters and prevent overfitting.
- **Test Set**: Used for final model evaluation.

## Exploratory Data Analysis (EDA)

Before model training, EDA is performed to gain insights into the dataset. Key aspects of the EDA include:
- **Class Distribution**: Analyzing the distribution of pneumonia and healthy images.
- **Pixel Intensity Analysis**: Understanding the range of pixel values in the images.
- **Image Size Analysis**: Checking for uniformity in image dimensions.
- **Representative Images**: Visualizing sample images to get a sense of the data.

## Model Architecture

### VGG19
The VGG19 model is used in this project with transfer learning. The key steps include:
- **Pre-trained Weights**: Using weights pre-trained on the ImageNet dataset.
- **Custom Classification Layer**: Adding custom layers on top of the base VGG19 model for pneumonia detection.
- **Data Augmentation**: Applied to improve model generalization.

## Training

The training process involves:
- **Optimization**: Using an appropriate optimizer (e.g., Adam) with a learning rate schedule.
- **Loss Function**: Binary cross-entropy is used for classification.
- **Early Stopping**: Implemented to prevent overfitting based on validation loss.
- **Metrics**: Accuracy and AUC (Area Under the Curve) are the primary metrics.

### Performance Metrics
- **Training AUC**: 99.9% with a loss of 0.08.
- **Validation AUC**: 100% with a loss of 0.13, indicating slight overfitting.
- **Test AUC**: 96% with accuracy of 92.6%, precision of 92.5%, recall of 95.9%, and F1 score of 94.2%.

## Results

The VGG19 model achieves satisfactory results:
- **Training Accuracy**: 95%
- **Validation Accuracy**: Slightly higher than training, but with signs of overfitting.
- **Test Performance**: AUC of 96% and accuracy of 92.6%, indicating the model's strong generalization capability.

These results suggest that the model is well-suited for real-world pneumonia diagnosis tasks.

## Conclusion

This project successfully demonstrates the application of deep learning, particularly transfer learning using VGG19, for pneumonia detection from chest X-ray images. The high performance metrics indicate the potential for deployment in clinical settings to assist healthcare professionals in rapid and accurate diagnosis.
