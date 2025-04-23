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
📁 data/ # Input datasets (ligands, descriptors, yields) 📁 notebooks/ # All Jupyter notebooks (preprocessing, ML, thresholding) 📁 combinatorial_design/ # Scripts for PA2B-based ligand generation 📁 fingerprints/ # Morgan fingerprint generation and conversion 📁 models/ # ML model files and scripts 📁 analysis/ # Yield–descriptor correlation and thresholding analysis 📄 README.md # Project description


---

## ⚙️ Installation

```bash
git clone https://github.com/alphago1234/Cross-Electrophile-Coupling.git
cd Cross-Electrophile-Coupling
pip install -r requirements.txt

🚀 Usage Guide
Preprocess Ligands
→ notebooks/Remove Ring.ipynb
Filters out phosphacyclic and invalid ligands.

Generate Features
→ notebooks/Generating Features.ipynb
Converts SMILES to 1024-bit Morgan fingerprints.

Train ML Model
→ notebooks/ML_DFT_Model_Training.ipynb
Trains XGBoost models for all 190 DFT descriptors.

Threshold Analysis
→ notebooks/Ligand Analysis Thresholding.ipynb
Identifies key descriptors that correlate with yield cutoffs.

Combinatorial Ligand Design
→ combinatorial_design/PA2B_Generator.py
Generates ~1200 new ligands using A–X–A–Y–B format and filters them.

Prediction & Screening
Apply ML model to predict descriptors → filter ligands based on thresholding → prioritize candidates for synthesis.

📊 Model Evaluation Summary

Model	Avg R²	Notes
XGBoost	0.86	Final model used for prediction
Random Forest	~0.5	Moderate, performance varies by feature
Gradient Boost	~0.6	Sensitive to hyperparameters
SVM / Ridge / Lasso	<0.4	Poor generalization for descriptor space
Gaussian Proc.	~0.65	Good with uncertainty quantification
Deep Learning	~0.7	Effective but resource-intensive
🧪 Experimental Outcome
Initial Testing: 37 ligands tested, yield range: 0–35%

ML-Driven Candidates: 6 new ligands selected post-thresholding

Best Ligand: 93% yield (surpassed all original candidates)




