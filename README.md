# Deep Learning Applications on Omics Data and Diagnostics

**M.Phil. Thesis | Kadir Has University — Computational Biology & Bioinformatics | 2018**

This repository contains the Jupyter Notebook implementations from my master's thesis, [*Deep Learning Applications on Biological Data*](Zeynep_Kurt_MSc_Thesis_Deep_Learning_Biological_Data_2018.pdf). The work applies Softmax Regression, Feed Forward Neural Networks (FFNN), and Long Short-Term Memory (LSTM) networks to four biological and medical datasets, demonstrating how increasing model complexity improves classification accuracy.

**Stack:** Python · TensorFlow · Keras · NumPy · Pandas · Scikit-learn · Matplotlib

---

## Notebooks

### Softmax Classification

| Notebook | Description |
|---|---|
| [Softmax_Multiclass_Classification_4Datasets.ipynb](Softmax_Classification/Softmax_Multiclass_Classification_4Datasets.ipynb) | Softmax multiclass classification on all four datasets (Anuran Call, Thyroid, E. coli, HIV) with min-max input normalization and loss/accuracy plotting |

### Softmax with Keras — Bias-Variance Tradeoff & Optimizer Comparison

| Notebook | Description |
|---|---|
| [Softmax_Keras_BiasVariance_Optimizer_Comparison.ipynb](Softmax_Keras_BiasVariance_LSTM/Softmax_Keras_BiasVariance_Optimizer_Comparison.ipynb) | Softmax on four datasets implemented in Keras; optimizer comparison (ADAM, SGD, RMSprop); bias-variance tradeoff analysis; introduces LSTM |

### Feed Forward Neural Networks & LSTM (Keras)

| Notebook | Description |
|---|---|
| [Anuran_Frog_Species_Softmax_Baseline.ipynb](FeedForward_Networks_and_LSTM/Frog/Anuran_Frog_Species_Softmax_Baseline.ipynb) | Softmax baseline for Anuran Call (frog species) classification — 15 classes, 22 MFCC features |
| [Anuran_Frog_Species_FFNN_Regularization.ipynb](FeedForward_Networks_and_LSTM/Frog/Anuran_Frog_Species_FFNN_Regularization.ipynb) | FFNN model selection and regularization (L2, Dropout) for frog species — accuracy improved from 78% to 95% |
| [Ecoli_Protein_Localization_Softmax.ipynb](FeedForward_Networks_and_LSTM/Ecoli_Protein_Localization_Softmax.ipynb) | Softmax classification for E. coli protein subcellular localization — 336 instances, 7 attributes, 8 classes |
| [HIV_Cleavage_FFNN_Model_Selection.ipynb](FeedForward_Networks_and_LSTM/HIV/HIV_Cleavage_FFNN_Model_Selection.ipynb) | FFNN model selection for HIV-1 protease cleavage site prediction — binary classification on 6,590 octamer sequences |
| [HIV_Cleavage_FFNN_Regularization.ipynb](FeedForward_Networks_and_LSTM/HIV/HIV_Cleavage_FFNN_Regularization.ipynb) | Regularization tuning (L2 and Dropout) on the best HIV FFNN model; final test set evaluation |

---

## Datasets

**Anuran Call** — 7,195 syllables from 60 audio recordings of 15 frog species; 22 MFCCs per syllable.

**Thyroid Patients** — 72,000 patient records with 21 clinical attributes; task: classify as healthy, hyperthyroid, or hypothyroid.

**E. coli Protein Localization** — 336 instances, 7 biophysical attributes; task: predict protein subcellular localization site (8 classes).

**HIV Cleavage Sites** — 6,590 amino acid octamer sequences (concatenated from four datasets); task: binary classification of HIV-1 protease cleavage sites.

---

## Results

| Dataset | Softmax | FFNN |
|---|---|---|
| Anuran (Frog Species) | 78% | 95% |
| Thyroid Patients | high | — |
| E. coli Localization | moderate | — |
| HIV Cleavage Sites | 81% | improved with LSTM |

---

## How to Run

```bash
pip install tensorflow keras numpy pandas scikit-learn matplotlib jupyter
jupyter notebook
```

---

## Background

Completed as part of the M.Phil. program in Computational Biology and Bioinformatics at Kadir Has University, Istanbul, under the supervision of Assoc. Prof. Cem Özen.
