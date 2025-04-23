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






