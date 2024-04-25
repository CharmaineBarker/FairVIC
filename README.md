# FairVIC
This repository contains code from my paper on **Fairness** through **V**ariance, **I**nvariance, and **C**ovariance.

### Introduction
yap yap yap

<p align="center">
  <img src="fairVIC.png" alt="High-level Overview of FairVIC" width="400"/>
</p>
<p align="center">Fig 1. A high-level overview of the FairVIC loss function in a neural network training loop.</p>

### FairVIC
yap yap yap

### Getting Started
All of the code and packages necessary to implement FairVIC are contained within a tutorial Jupyter Notebook in this repository. This notebook will guide you step by step into using FairVIC in a standard neural network. We encourage you to tweak parameters, weights, and models to highlight the power of FairVIC.

### Files
This repository contains the following files:
* `ECAISupplementaryCode.ipynb` - A detailed Jupyter Notebook that will guide readers through using FairVIC.
* `fairVIC.png` - A high-level overview image of how FairVIC is incorporated within the training of a neural network.

### Datasets
We evaluate FairVIC in our paper on three tabular datasets that are used in bias mitigation evaluation due to their known biases towards certain subgroups of people within their sample population. These datasets allow for highlighting the generalisable capabilities of FairVIC across different demographic disparities.

Dataset 1: [Adult Income](https://archive.ics.uci.edu/dataset/2/adult).
This is the primary dataset we use for our evaluation. The classification task is to predict whether an individual's income is >$50K or ≤$50K. It is particularly known for its gender and racial biases in economic disparity.

Dataset 2: [COMPAS](https://www.propublica.org/datastore/dataset/compas-recidivism-risk-score-data-and-analysis).
The Correctional Offender Management Profiling for Alternative Sanctions (COMPAS) dataset is frequently used for evaluating debiasing techniques. It has a classification goal of predicting recidivism risks and is infamous for its racial biases.

Dataset 3: [German Credit](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data). 
This final dataset is used to assess creditworthiness by classification of individuals into bad or good credit risks, with known biases related to age and gender. 

Metadata for each of the three datasets can be seen below:
| Dataset                  | Adult        | COMPAS           | German        |
| -------------            | ------------ | -------------    | ------------- |
| No. of Features          | 11           | 8                | 20            |
| No. of Rows              | 48,842       | 5,278            | 1,000         |
| Target Variable          | income       | two_year_recid   | credit        |
| Favourable Label         | >50K (1)     | False (0)        | Good (1)      |
| Unfavourable Label       | <=50K (0)    | True (1)         | Bad (0)       |
| Protected Characteristic | sex          | race             | age           |
| Privileged Group         | male (1)     | Caucasian        | >25 (1)       |
| Unprivileged Group       | female (0)   | African-American | <=25 (0)      |
