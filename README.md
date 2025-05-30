# 3D U-Net for Brain Tumor Segmentation (BraTS 2020)

This project implements a 3D U-Net model enhanced with Spatial Attention and SpatialDropout3D for precise brain tumor segmentation using the BraTS 2020 dataset. The model is trained to segment different tumor subregions from multi-modal MRI scans.

![Model Architecture](results/architecture.png)

---

## 🧠 Overview

Accurate brain tumor segmentation is critical for diagnosis, treatment planning, and follow-up. Our model integrates attention mechanisms and regularization techniques into a 3D U-Net to better capture tumor boundaries and reduce overfitting.

---

## 🗂️ Dataset

- **Dataset:** [BraTS 2020](https://www.med.upenn.edu/cbica/brats2020/)
- **Modalities Used:** FLAIR, T1, T1CE
- **Tumor Classes:**
  - `0`: Background (Non-tumor)
  - `1`: Necrotic/Core
  - `2`: Edema
  - `3`: Enhancing Tumor

> ⚠️ Due to licensing restrictions, the dataset is not included. Please download it manually from the [BraTS 2020 website](https://www.med.upenn.edu/cbica/brats2020/).

---

## 📁 Project Structure

