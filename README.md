# Liver Segmentation Using 3D U-Net

This project implements liver segmentation using the 3D U-Net deep learning architecture, provided by Monai, which is specifically designed for biomedical imaging tasks. The purpose of this project is to perform semantic segmentation of liver scans from medical imaging datasets.

## Project Overview

- **Goal**: Implement liver segmentation using a 3D U-Net model.
- **Method**: Semantic segmentation with supervised learning, utilizing the Monai library for medical imaging.
- **Data Preparation**: Tools like 3D Slicer and ITK-SNAP were used for preparing and visualizing the dataset, ensuring correct format and consistency for the model.
- **Model Training**: Custom scripts were used to train the model, with the Dice coefficient as the evaluation metric.
- **Status**: Currently in the model training phase, aiming to complete the project within the week.

## Steps Involved

### 1. Data Preparation
- The dataset used for this project is the liver tumor segmentation dataset from Kaggle.
- **Preprocessing Tools**: 3D Slicer, ITK-SNAP.
- **File Formats**: Data was converted between DICOM and Nifti formats to prepare for segmentation.
- **Image Grouping**: Grouped image slices to ensure each 3D input volume has the same dimensions (number of slices per group).
- **Filtering**: Removed patient data with missing segmentations or volumes.
- **Preprocessing**: 
  - Resized input images.
  - Adjusted image contrast to make organs distinguishable using ITK-SNAP.

### 2. Model Architecture
- **Model**: 3D U-Net based on Monai, tailored for semantic segmentation in medical imaging.
- **Loss Function**: Dice Loss.
- **Metrics**: Dice coefficient for segmentation accuracy.

### 3. Training and Validation
- **Training**: The model is trained over several epochs, tracking training and validation losses.
- **Validation**: At specified intervals, the model is validated using the Dice metric, and the best-performing model is saved.
- **Metrics Tracking**: Both training and validation losses, along with Dice scores, are tracked throughout the process.

## Tools & Libraries
- **Monai**: For model development and medical imaging tasks.
- **PyTorch**: Deep learning framework for model training.
- **NumPy**, **Pandas**: For data manipulation.
- **Matplotlib**: For visualizing results.
- **3D Slicer**, **ITK-SNAP**: Used for data preparation, visualization, and contrast adjustment.

## Current Status
- **Data Preparation & Preprocessing**: Completed.
- **Model Training**: In progress, using custom scripts to fine-tune the model with Dice loss and track performance.

## Next Steps
- Complete the training phase.
- Perform validation and evaluate final model performance.
- Save the best model based on the highest Dice score.

## Acknowledgments
- Kaggle for providing the liver tumor segmentation dataset.
- Monai and PyTorch for the deep learning frameworks used in this project.
