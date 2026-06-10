# Smoking Status Classification Using Human Oral Transcriptomic Data

## Overview

This project investigates whether smoking status can be predicted from human gene expression profiles using machine learning.

Using publicly available transcriptomic data from GEO (GSE17913), a Random Forest classifier was trained to distinguish smokers from never-smokers based on oral mucosal gene expression patterns.

## Dataset

**Dataset:** GSE17913

**Platform:** GPL570 (Affymetrix Human Genome U133 Plus 2.0 Array)

**Samples:**

* Never smokers: 40
* Smokers: 39

Total samples analysed: 79

## Methods

* Downloaded and processed GEO Series Matrix data
* Extracted smoking-status labels from sample metadata
* Constructed a transcriptomic feature matrix
* Selected the top 500 informative features
* Trained a Random Forest classifier
* Evaluated performance on unseen test samples

## Results

| Metric            | Value  |
| ----------------- | ------ |
| Accuracy          | 87.5%  |
| Samples           | 79     |
| Initial Features  | 54,675 |
| Selected Features | 500    |

### Confusion Matrix

See `results/confusion_matrix.png`

## Key Findings

Gene expression profiles from oral mucosal tissue contain sufficient biological signal to distinguish smokers from never-smokers with high classification accuracy.

## Tools Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Google Colab
* GEO

## Future Improvements

* Map probe IDs to gene symbols
* Perform pathway enrichment analysis
* Compare multiple machine learning models
* Validate findings using independent datasets
