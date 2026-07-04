# EEG-based Classification of First-Episode Psychosis (FEP)

## Goal
Classify first-episode psychosis (FEP) using EEG signals and machine learning models.

## Data
Two public OpenNeuro datasets combined: 143 subjects (82 FEP, 61 controls).

## Methods
- Preprocessing: filtering, bad channel removal, artifact removal (ICA), PSD analysis.
- Feature extraction (38 features per EEG channel), resulting in "eeg_features" dataset.
- Feature engineering: spectral ratios, hemispheric asymmetries, topographic gradients.  
- Feature selection: L1-penalized logistic regression (Lasso).  
- Models: Dummy (baseline), Logistic Regression, KNN, and Random Forest, optimized with StratifiedKFold cross-validation.  
- Evaluation: ROC-AUC, accuracy, sensitivity, specificity, and F1-score.

## Main Results
- Random Forest achieved AUC ≈ 0.65.  
- Key features: statistical metrics, asymmetries, and gradients.  
- Small sample (n=143) and high dimensionality suggest that more data could improve performance.

## Run the Notebook
1. Clone this repo.  
2. Install dependencies: `pip install -r requirements.txt`.  
3. Open and run `notebooks/MVP.ipynb` (Google Colab or Jupyter).

## License
MIT.

## Data Source
OpenNeuro

## Contact
Pedro Fortes
https://github.com/pedrof0rtes
https://www.linkedin.com/in/pedro-fortes-psi/
