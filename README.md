# Cross-Electrophile-Coupling
ML Driven Ligand Discovery
# 🧪 ML-Driven Ligand Discovery for Cross-Electrophile Coupling

This repository contains the full pipeline for phosphine ligand optimization using machine learning and DFT descriptor prediction. We integrate quantum-calculated descriptors, combinatorial ligand generation, XGBoost modeling, and experimental validation to accelerate the design of effective ligands for Br–OTf cross-coupling.

---

## 📌 Highlights

- 🔬 **Dataset**: 1,550 ligands (Kraken dataset), 190 DFT descriptors per ligand (steric + electronic)
- 🧠 **Model**: XGBoost trained on Morgan fingerprints to predict descriptors
- ⚙️ **Performance**: R² ≈ 0.86, MAE ≈ 5.0 on validation set
- 🧪 **Validation**: Top 6 ligands from thresholding tested; highest yield reached **93%**
- 📈 **Thresholding**: Yield vs descriptor analysis to find critical property cutoffs

---

## 📁 Repository Structure


