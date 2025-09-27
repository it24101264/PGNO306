##  Project Overview

This project focuses on cleaning, preprocessing, and balancing the **Loan Default dataset** to prepare it for machine learning models. The pipeline covers:

- Data cleaning (handling missing values, duplicates)
- Outlier detection and winsorization
- Label encoding categorical features
- Train-test split and SMOTE balancing
- Standardization of numerical features
- Feature importance analysis (Random Forest)
- Class balancing via **Oversampling, Undersampling, and SMOTE**
- Saving cleaned datasets and visualizations

---

##  Repository Structure

PGNO306/
│
├── data/
│ ├── raw/ # Original dataset (Loan_Default.csv)
│ └── alter/ # Cleaned / processed versions (optional)
│
├── results/
│ ├── EDA Visuals/ # Boxplots, class distribution plots, feature importances
│ └── outputs/ # Balanced datasets (oversample/undersample/SMOTE)
│
├── notebooks/ # Jupyter Notebooks for each step
│ ├── dataCleaning.ipynb
│ ├── outliersHandling.ipynb
│ ├── encodingData.ipynb
│ ├── dataScaling.ipynb
│ ├── dataResampling.ipynb
│ ├── featureSelection.ipynb
│ └── pipeline.ipynb # End-to-end workflow
│
└── README.md # Project documentation

Always show details

---

##  Preprocessing Steps

### 1. **Data Cleaning**

- Removed duplicates.
- Filled missing categorical values with `"Unknown"`.
- Dropped rows where `age` was missing.
- Filled missing numerical values with **median**.

### 2. **Outlier Handling (Winsorization)**

- Applied **IQR method** to cap extreme values.
- Generated boxplots (saved in `EDA Visuals/`).

### 3. **Encoding**

- Converted categorical features to numeric using **Label Encoding**.
- Stored mappings for reproducibility.

### 4. **Class Balancing**

- Split dataset into **train-test** with stratification.
- Applied **SMOTE** for synthetic oversampling of minority class.
- Also tested:
  - **Random Oversampling** (duplicate minority samples).
  - **Random Undersampling** (reduce majority samples).
- Plots of class distributions are saved.

### 5. **Scaling**

- Standardized numerical features using **StandardScaler**.

### 6. **Feature Selection**

- Trained **Random Forest Classifier**.
- Ranked features by importance.
- Saved top 20 feature importance plot.

---

##  Outputs

- **Plots (in `EDA Visuals/`)**

  - Boxplots (after outlier handling)
  - Class distributions before/after SMOTE
  - Feature importance bar plot

- **Balanced Datasets (in `results/outputs/`)**
  - `df_downsampled.csv` – undersampled dataset
  - `df_upsampled.csv` – oversampled dataset
  - `X_train_sm.csv`, `y_train_sm.csv` – SMOTE-balanced training data

---
