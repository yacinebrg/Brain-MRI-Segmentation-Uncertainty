# Brain-MRI-Segmentation-Uncertainty
Segmentation of Cerebral Tissues in Human Brain MRIs with uncertainty

- Author: Yacine CADI-BOUREGHDA
- Supervisor: Nicolas BOUTRY
- Date: Jan 2025
- Technical Report: no202501-techrep-boureghda

Project Overview

This repository contains the code and resources for the project titled Segmentation of Cerebral Tissues in Human Brain MRIs with Uncertainty. The goal of this project is to develop a neural network model that performs segmentation on MRI images of human brains, specifically for detecting and analyzing tumor progression across voxels. The model also provides uncertainty quantification through two advanced techniques: Monte Carlo Dropout (MCD) and Deep Ensembles (DE).

The purpose of uncertainty quantification is to understand the model's confidence in its predictions and detect areas where the model might be uncertain, especially in noisy or ambiguous data.

Key Methods

1. Monte Carlo Dropout (MCD)
Monte Carlo Dropout is a technique that generates multiple predictions by applying dropout during both training and inference. The variance in the predictions helps to estimate the uncertainty related to the model's parameters.

2. Deep Ensembles (DE)
Deep Ensembles involve training multiple models with different initializations. By aggregating predictions from multiple models, DE allows us to capture uncertainty that arises from different model parameterizations.

3. Hybrid Approach (MCD + DE)
A combination of MCD and DE methods is used to test if this hybrid approach improves uncertainty quantification by leveraging both stochastic predictions from MCD and diversity from multiple models in DE.

Datasets

The project primarily uses the iSEG-2017 dataset, which consists of high-resolution MRI scans of infant brains. The dataset contains ground truth annotations for white matter, gray matter, and cerebrospinal fluid (CSF). These annotations allow for accurate segmentation and provide a basis for assessing the performance of segmentation models.

Results

The results of the segmentation and uncertainty estimation are saved and can be visualized in the provided notebooks. The Monte Carlo Dropout and Deep Ensembles methods show how uncertainty varies in different brain regions and can be used to assess the reliability of the model's predictions.

Links

## Links

The full research report for my project is available [here](./docs/202501_techrep_BOUREGHDA.pdf).
