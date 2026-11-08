# DSCI 552 — Homework 6

Tree-based methods on the UCI APS Failure at Scania Trucks data (median imputation, coefficient of variation, correlation matrix, visualization of the highest-CV features, random forests with and without compensation for class imbalance, L1-regularized XGBoost, and SMOTE applied to the full training set with SMOTE inside cross-validation), plus the ISLR exercises 6.6.3, 6.6.5, 8.4.5 and 9.7.3.

## Structure

```
.
├── README.md
├── .gitignore
├── data
│   └── aps_failure
│       ├── aps_failure_description.txt
│       ├── aps_failure_test_set.csv
│       └── aps_failure_training_set.csv
├── notebook
│   └── Lu_Yiming_HW6.ipynb
└── requirements.txt
```

## Run

```bash
pip install -r requirements.txt
cd notebook
jupyter notebook Lu_Yiming_HW6.ipynb   # then Kernel -> Restart & Run All
```

The notebook loads data with the relative path `../data/aps_failure/`. Each CSV file starts with a 20-line license header and codes missing values as `na`; the notebook reads it accordingly. A full run (three 300-tree random forests, two 5-fold cross-validations of XGBoost over six values of alpha, SMOTE on all 60,000 training rows) takes several minutes on a multi-core machine.
