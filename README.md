# Precision Medicine ML Pipeline (Gene Expression)

This project demonstrates an end-to-end machine learning workflow
inspired by transcriptomic precision medicine studies.

The pipeline simulates gene expression data, applies biologically
motivated preprocessing, performs feature selection, and trains
classification models to identify disease status.

---

## Dataset Description

- Simulated gene expression counts (Poisson-distributed)
- Samples: 50 patients
- Features: 100 genes
- Label:
  - 0 = Healthy
  - 1 = Infected

This setup mimics RNA-seq / qPCR-style count data commonly used in
biomedical research.

---

## Pipeline Overview

1. Gene expression simulation
2. Log-normalization
3. Train-test split
4. Feature selection (variance threshold)
5. Logistic Regression classification
6. Random Forest classification
7. Feature importance analysis

---

## Results

- Logistic Regression achieved ~60% accuracy on held-out data,
  outperforming random baseline.

- Random Forest modeling identified a small panel of genes driving
  disease prediction.

Top contributing genes:
- Gene_20
- Gene_18
- Gene_6
- Gene_7
- Gene_13

Gene_20 alone contributed ~29% of total model decision-making,
consistent with polygenic disease architectures observed in
real-world transcriptomic studies.

---

## Key Biological Insight

Variance-based feature selection must be applied prior to
standardization. Applying variance filtering after z-score
normalization removes meaningful biological signal.

This reflects a common pitfall in transcriptomics pipelines.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- scikit-learn
- Jupyter Notebook

---

## Future Work

- PCA visualization of expression profiles
- ROC-AUC analysis
- Cross-validation
- Integration with real RNA-seq datasets

---

## Author

Goudham Baskar  
MSc Graduate | Biomedical & Genomic Data Analysis  

