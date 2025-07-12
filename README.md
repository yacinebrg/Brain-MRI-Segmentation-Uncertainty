# Brain-MRI-Segmentation-Uncertainty

**Segmentation of Cerebral Tissues in Human Brain MRIs with Uncertainty**

- **Author**: Yacine CADI-BOUREGHDA  
- **Supervisor**: Nicolas BOUTRY  
- **Date**: Jan 2025  
- **Technical Report**: [no202501-techrep-boureghda](./docs/202501_techrep_BOUREGHDA.pdf)

---

## Project Overview

This repository contains the code and resources for the project **Segmentation of Cerebral Tissues in Human Brain MRIs with Uncertainty**. This research is part of my work at the **EPITA Research Laboratory**, within the **Computer Vision / Artificial Intelligence team**.

The aim of this project is to develop a neural network capable of performing segmentation on MRI images of human brains, specifically for detecting and analyzing tumor progression across different brain regions. In addition to segmentation, this work also focuses on **uncertainty quantification** through two advanced techniques:

1. **Monte Carlo Dropout (MCD)**: This method generates multiple predictions by applying dropout during both training and inference, allowing for the estimation of uncertainty associated with the model's parameters.

2. **Deep Ensembles (DE)**: This technique involves training multiple models with different initializations, and combining their predictions to capture the uncertainty arising from different model parameterizations.

3. **Hybrid Approach (MCD + DE)**: We combine the MCD and DE methods to evaluate whether this hybrid approach improves uncertainty quantification by leveraging both stochastic predictions from MCD and diversity from multiple models in DE.

The purpose of uncertainty quantification is to better understand the model's confidence in its predictions and to identify areas where the model might be uncertain, especially when dealing with noisy or ambiguous data.

---

## Key Methods

### 1. **Monte Carlo Dropout (MCD)**
Monte Carlo Dropout is a technique that helps quantify uncertainty in neural networks by applying dropout at inference time. By generating multiple predictions with random dropout, the model's uncertainty can be estimated from the variance in these predictions.

### 2. **Deep Ensembles (DE)**
Deep Ensembles involve training multiple neural networks with different random initializations. By aggregating predictions from these independently trained models, we capture the uncertainty arising from the diversity of model parameterizations.

### 3. **Hybrid Approach (MCD + DE)**
This approach combines the power of MCD and DE to improve uncertainty estimation. The hybrid method leverages both the stochastic nature of dropout and the model diversity from the ensemble approach to better quantify uncertainty.

---

## Datasets

This project primarily uses the **iSEG-2017 dataset**, which consists of high-resolution MRI scans of infant brains. The dataset includes ground truth annotations for **white matter**, **gray matter**, and **cerebrospinal fluid (CSF)**. These annotations enable accurate segmentation, providing a foundation for evaluating the performance of segmentation models.

---

## Results

The results of segmentation and uncertainty estimation are saved and can be visualized in the provided Jupyter notebooks. The **Monte Carlo Dropout** and **Deep Ensembles** methods show how uncertainty varies across different brain regions, which can be used to assess the reliability of the model's predictions.

---

## Links

The full research report for my project is available [here](./docs/202501_techrep_BOUREGHDA.pdf).

---

## Getting Started

To explore the project and view the results, open the Jupyter Notebook provided in this repository. The notebook contains:
- **Segmentation Results**: Visualizations of the segmented brain tissues.
- **Uncertainty Estimations**: Maps displaying the uncertainty in the segmentation results, with both **epistemic** and **aleatoric** uncertainties quantified.

---

## License

This project is licensed under the terms of the GNU Free Documentation License, Version 1.2 or any later version.

---

Feel free to contribute or raise issues if you encounter any problems. You can contact me via email: **yacine.boureghda@epita.fr**.

