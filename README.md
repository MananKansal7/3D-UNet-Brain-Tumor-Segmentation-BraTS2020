# Brain Tumor Segmentation Using 3D U-Net (BraTS 2020)

This repository contains a deep learning project that uses a 3D U-Net architecture with Spatial Attention and SpatialDropout3D for segmenting brain tumors from MRI scans. The model is trained on the BraTS 2020 dataset.

---

## Overview

Brain tumor segmentation is a critical step in medical image analysis. This project enhances the basic 3D U-Net by integrating spatial attention and dropout to improve focus on important tumor regions and reduce overfitting.

---

## Dataset

- Dataset: BraTS 2020
- Modalities used: FLAIR, T1, T1CE
- Classes:
  - 0: Background (non-tumor)
  - 1: Necrotic/Core
  - 2: Edema
  - 3: Enhancing Tumor

Note: Due to license restrictions, the dataset is not included. Download it from the official website: https://www.med.upenn.edu/cbica/brats2020/

---

## Project Structure

project/
│
├── data/ # Dataset (not included)
├── src/
│ ├── model.py # 3D U-Net + Attention
│ ├── data_generator.py # Data pipeline
│ ├── train.py # Training script
│ ├── inference.py # Prediction script
│ └── utils.py # Evaluation and helpers
├── results/
│ ├── predictions/ # Output predictions
│ └── checkpoints/ # Model weights
├── demo.ipynb # Jupyter notebook version
├── requirements.txt
├── README.md
└── .gitignore

---

## Installation

Install the required Python packages using:


Main dependencies:
- TensorFlow
- Keras
- nibabel
- matplotlib
- scikit-learn

---

## Training

To train the model:


This script uses multi-GPU training with MirroredStrategy and logs performance metrics.

---

## Inference

To run predictions on test images:


---

## Results

Example Dice scores for different tumor classes:

| Tumor Class       | Dice Score |
|-------------------|------------|
| Necrotic/Core     | 0.87       |
| Edema             | 0.91       |
| Enhancing Tumor   | 0.89       |

Update with your own results if needed.

---
