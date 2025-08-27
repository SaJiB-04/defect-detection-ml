# Defect Detection in Manufacturing using Machine Learning

This repository contains the implementation of my research project on **predicting manufacturing defects using machine learning classifiers**.  
The project was developed in Python (Jupyter Notebook) and later submitted as a paper to **IEEE COMPSAC 2025**.

---

## 🔹 Problem Statement
Defects in manufacturing increase costs, cause delays, and can lead to safety issues or recalls.  
Traditional quality control methods rely on static thresholds or manual inspection, which often fail to capture complex defect patterns.  

This project applies **supervised machine learning** to predict defect status (defective or non-defective) using production process data, enabling **data-driven quality assurance** in Industry 4.0 environments.

---

## 🔹 Dataset
- **Source**: Kaggle (Predicting Manufacturing Defects Dataset)  
- **Samples**: 3,240 production instances  
- **Features**: 16 operational metrics (e.g., ProductionVolume, MaintenanceHours, DowntimePercentage, SupplierQuality, EnergyEfficiency)  
- **Target Variable**: `DefectStatus` → Defective (1) or Non-defective (0)  
- **Class Distribution**: Imbalanced (2695 defective, 545 non-defective)

---

## 🔹 Methods
Three classifiers were trained, tested, and compared:
- **Logistic Regression** – Linear baseline model  
- **Decision Tree** – Rule-based, interpretable model  
- **Random Forest** – Ensemble of trees for robust classification  

### Preprocessing
- Checked for missing values (none found)  
- Feature standardization (for Logistic Regression)  
- Train-test split (80:20, stratified to preserve class balance)  

---

## 🔹 Results
| Model              | Accuracy (%) | F1-Score (Class 0) | F1-Score (Class 1) |
|--------------------|--------------|---------------------|---------------------|
| Logistic Regression| 87.65        | 0.49                | 0.93                |
| Decision Tree      | 89.97        | 0.69                | 0.94                |
| **Random Forest**  | **95.06**    | **0.82**            | **0.97**            |

- **Best Model**: Random Forest  
- **Key Insights**:
  - Random Forest minimized **false negatives (0.7%)** and reduced **false positives** significantly.  
  - Top predictive features:
    - **Production Volume**
    - **Downtime Percentage**
    - **Maintenance Hours**

---

## 🔹 Visual Results
- Accuracy comparison across classifiers  
- F1-score comparison per class  
- Confusion matrices for each model  
- Feature importance (Random Forest)  

👉 See the `results/` folder for figures and metrics.

---

## 🔹 Repository Contents
- `notebooks/` → Jupyter notebook (`defect_detection.ipynb`)  
- `results/` → Model metrics and plots (`metrics.txt`, `confusion_matrix.png`, `feature_importance.png`)  
- `data/` → Dataset notes (real dataset available on Kaggle)  
- `paper/` → Submitted IEEE paper:  
  [Predictive Modelling of Manufacturing Defects Using Machine Learning Classifiers (IEEE COMPSAC 2025 Submission)](paper/ZubaerRahman_DefectPrediction_COMPAS2025.pdf)  
- `requirements.txt` → Required Python libraries  
- `.gitignore` → Ignore cache and notebook checkpoint files  

---

## 🔹 How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
2. Open the notebook:
    ```bash
   jupyter notebook notebooks/defect_detection.ipynb

## 🔹 Citation

If you use this work, please cite:

Md. Zubaer Rahman Sajib,
"Predictive Modelling of Manufacturing Defects Using Machine Learning Classifiers,"
submitted to IEEE COMPSAC 2025.

## 🔹 Author

Md. Zubaer Rahman Sajib,
B.Sc. in Industrial & Production Engineering, KUET
Email: zubaer.rahman2000@gmail.com
