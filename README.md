# GeneRA - Rheumatoid Arthritis Prediction

Predicting Rheumatoid Arthritis (RA) from gene expression data using Machine Learning / Deep Learning.

## Dataset
- RA: GSE97810 (RA-MAP cohort)
- Control: GSE97475 (Healthy cohort)
- Platform: GPL10904
- Tissue: PBMC
- Total: 280 samples (245 RA, 35 Control)

## Pipeline
1. Download data with GEOparse
2. Clean metadata & deduplicate by participant
3. Train-Test Split (80/20, stratified)
4. Feature Selection (SelectKBest, Top 300 genes)
5. Scaling (StandardScaler - fit on train only)
6. Model: Neural Network (Dense 128 -> 64 -> 1)

## Results (Sample Project)
- Accuracy: 1.00
- Precision: 1.00
- Recall: 1.00

> Note: RA and Control come from different GEO series, so performance may be inflated due to batch effect. For a real clinical model, validation on an independent cohort is required.

## Tech Stack
Python, Google Colab, GEOparse, scikit-learn, TensorFlow / Keras
