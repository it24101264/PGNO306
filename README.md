# Loan Data Preprocessing & Analysis Pipeline

This project contains Jupyter notebooks and scripts for **cleaning, preprocessing, resampling, and feature selection** on a loan dataset.  
The workflow follows a modular pipeline approach, with each step separated into a dedicated notebook.

---

## Project Structure

PGNO306/
│
├── data/                        # Raw and altered datasets
│   ├── raw/                     # Original input data
│   └── alter/                   # Modified / cleaned data
│
├── notebooks/                   # Step-by-step processing notebooks
│   ├── dataCleaning.ipynb                 # Handle missing values, duplicates, inconsistencies
│   ├── IT2410186_outliarsHandling.ipynb   # Outlier detection and winsorization
│   ├── IT24101232_encodingData.ipynb      # Encode categorical variables
│   ├── dataScaling.ipynb                  # Scale numerical features
│   ├── IT24101264_dataResampling.ipynb    # Handle class imbalance (SMOTE, over/undersampling)
│   ├── IT24100760_featureSelection.ipynb  # Feature importance (embedded methods)
│   ├── classBalancing.ipynb               # Alternative class balancing experiments
│   ├── eda.ipynb                          # Exploratory Data Analysis
│   └── pipeline.ipynb                     # End-to-end pipeline (all steps combined)
│
├── results/
│   ├── EDA Visuals/              # Saved plots (boxplots, histograms, etc.)
│   ├── logs/                     # Logs from runs
│   └── outputs/                  # Resampled datasets
│       ├── df_downsampled.csv
│       ├── df_upsampled.csv
│       ├── X_train_sm.csv
│       └── y_train_sm.csv
│
└── README.md                     # Project documentation (this file)




---

## Workflow Overview

1. **Data Cleaning (`dataCleaning.ipynb`)**

   - Remove duplicates
   - Handle missing values
   - Basic fixes for column consistency

2. **Outlier Handling (`IT2410186_outliarsHandling.ipynb`)**

   - Winsorization
   - Boxplot checks

3. **Encoding (`IT24101232_encodingData.ipynb`)**

   - Convert categorical variables to numeric (Label/One-hot encoding)

4. **Scaling (`dataScaling.ipynb`)**

   - Standardization / MinMax scaling for numeric features

5. **Resampling (`IT24101264_dataResampling.ipynb`)**

   - Random oversampling / undersampling
   - SMOTE (synthetic minority oversampling)

6. **Feature Selection (`IT24100760_featureSelection.ipynb`)**

   - Embedded methods: Logistic Regression (L1), Random Forest
   - Top features plotted

7. **Exploratory Data Analysis (`eda.ipynb`)**

   - Distribution plots, correlations, approval rates by feature

8. **Pipeline (`pipeline.ipynb`)**
   - Full process from raw data → cleaned → resampled → selected features

---

## Results

- **EDA Visuals/** → Boxplots, histograms, and other plots saved automatically.
- **outputs/** → Balanced datasets for modeling:
  - `df_downsampled.csv` → After random undersampling
  - `df_upsampled.csv` → After random oversampling
  - `X_train_sm.csv` & `y_train_sm.csv` → After SMOTE resampling

---
