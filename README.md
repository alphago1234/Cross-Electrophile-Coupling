# 🧪 ML-Driven Ligand Discovery for Cross-Electrophile Coupling

This repository presents a machine learning-based framework for discovering high-performing phosphine ligands in Br–OTf cross-coupling reactions. We combine quantum mechanical descriptors, fingerprint-based models, and experimental testing to identify ligands that achieve yields as high as 93%.


## 📌 Highlights

- 📊 1,550 ligands analyzed using 190 DFT descriptors (steric + electronic)
- 🧠 XGBoost model trained on Morgan fingerprints with R² ≈ 0.86
- 🔍 Threshold analysis to identify key yield-driving features
- 🧪 Experimental testing validated 6 ligands, best yield: **93%**

## 📁 Repository Structure

- `data/` – Raw ligand dataset and DFT descriptors  
- `notebooks/` – Jupyter notebooks for preprocessing, training, and thresholding  
- `combinatorial_design/` – Scripts for fragment recombination (PA2B format)  
- `fingerprints/` – Morgan fingerprint generation tools  
- `models/` – ML model training and output files  
- `analysis/` – Scripts for feature threshold evaluation  


## ⚙️ Installation

```bash
git clone https://github.com/alphago1234/Cross-Electrophile-Coupling.git
cd Cross-Electrophile-Coupling
pip install -r requirements.txt

## 📊 Model Evaluation

| Model             | Avg R² | Notes                                  |
|------------------|--------|----------------------------------------|
| XGBoost          | 0.86   | Final model used for predictions       |
| Random Forest    | ~0.5   | Varies by descriptor                   |
| Gradient Boosting| ~0.6   | Sensitive to tuning                    |
| Deep Learning    | ~0.7   | Accurate but computationally heavy     |




