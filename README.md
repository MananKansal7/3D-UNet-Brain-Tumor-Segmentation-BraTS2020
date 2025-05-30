# 3D U-Net for Brain Tumor Segmentation (BraTS 2020)

This project implements a 3D U-Net model enhanced with Spatial Attention and SpatialDropout3D for precise brain tumor segmentation using the BraTS 2020 dataset. The model is trained to segment different tumor subregions from multi-modal MRI scans.

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

brain-tumor-segmentation/
│
├── data/ # Dataset (not included)
├── src/
│ ├── model.py # 3D U-Net + Spatial Attention
│ ├── data_generator.py # Custom data generator
│ ├── train.py # Training script
│ ├── inference.py # Prediction script
│ └── utils.py # Metrics, visualization, etc.
├── results/
│ ├── sample_predictions/ # Predicted mask overlays
│ └── model_checkpoints/ # Trained models
├── notebooks/
│ └── demo.ipynb # Colab demo notebook
├── paper/ # Research paper (optional)
│ └── BrainTumorSegmentation.pdf
├── requirements.txt
├── README.md
└── .gitignore

yaml
Copy
Edit

---

## ⚙️ Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
Key Libraries:

TensorFlow

Keras

nibabel

matplotlib

numpy

scikit-learn

🚀 Training
bash
Copy
Edit
python src/train.py
The training script uses MirroredStrategy for multi-GPU support and logs metrics like Dice score, precision, sensitivity, and specificity.

🔍 Inference
bash
Copy
Edit
python src/inference.py
Outputs segmented MRI slices with overlays for visual analysis.

📊 Results
Class	Dice Score	Precision	Sensitivity	Specificity
Necrotic/Core	0.87	0.90	0.85	0.95
Edema	0.91	0.92	0.90	0.97
Enhancing Tumor	0.89	0.91	0.88	0.96

(These are example results; replace with your actual numbers)

📸 Sample Predictions
Include sample images in results/sample_predictions/ and link here:

arduino
Copy
Edit
<img src="results/sample_predictions/example1.png" width="400"/> <img src="results/sample_predictions/example2.png" width="400"/>
✍️ Citation
If you use this code or model in your research, please cite:

java
Copy
Edit
@misc{yourgithubhandle2025brats,
  title={3D U-Net for Brain Tumor Segmentation (BraTS 2020)},
  author={Your Name},
  year={2025},
  url={https://github.com/yourusername/3D-UNet-Brain-Tumor-Segmentation-BraTS2020}
}
📜 License
This project is licensed under the MIT License.

🙏 Acknowledgements
BraTS 2020 Challenge

TensorFlow/Keras

U-Net and attention research community

yaml
Copy
Edit

---




