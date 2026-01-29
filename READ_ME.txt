# Lesion Prodromal Activity Classification from FLAIR MRI using Radiomics

This repository provides a reproducible pipeline to:

1. Extract radiomic features from FLAIR MRI lesion masks  
2. Classify lesions according to their prodromal activity using a pre-trained SVM model  
3. Visualize all lesions of a patient in 3D over the MRI volume  

The model classifies lesions as:
- Ls-E: Long-standing established lesions  
- R-I: Recent-incident lesions  

---

## Repository Structure

Files included in this repository:

- lesions_test_t0.csv
Example input file containing lesion metadata for one patient
(columns include: patient_id, lesion_id, lesion_mask_t0_path, t0_FLAIR_path)

- svm_radiomics_final.pkl
Pre-trained SVM classifier used for lesion classification

- params.yaml
PyRadiomics configuration file defining feature extraction settings

- output_model_example.ipynb
End-to-end example notebook demonstrating radiomic feature extraction, model inference and 3D lesion visualization over FLAIR MRI

- README.md

---

## Requirements

### Python
- Python ≥ 3.8 (tested with Python 3.8.20)

### Python packages

Core dependencies:

- numpy (≥ 1.24) — tested with 1.24.4
- pandas (≥ 2.0) — tested with 2.0.3
- SimpleITK (≥ 2.1) — tested with 2.1.1.1
- pyradiomics (≥ 3.1) — tested with 3.1.0
- scikit-learn (≥ 1.3) — tested with 1.3.2
- joblib (≥ 1.4) — tested with 1.4.2
- tqdm (≥ 4.67) — tested with 4.67.1
- matplotlib (≥ 3.7) — tested with 3.7.2

Optional (for 3D visualization):
- pyvista (≥ 0.44) — tested with 0.44.2
- FSL (BET) — tested with FSL 6.0.7.15