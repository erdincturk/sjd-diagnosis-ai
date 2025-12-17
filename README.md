# Diagnostic Performance of Deep Learning Models Using Parotid Gland Ultrasonography in Sjögren's Disease

This repository contains the official code implementation for the paper:
**"Diagnostic Performance of Deep Learning Models Using Parotid Gland Ultrasonography in Sjögren's Disease"**
*Submitted to Biomedical Signal Processing and Control (BSPC)*

## 📄 Overview
This project evaluates lightweight deep learning models (specifically **YOLO11s-cls**) for the automated diagnosis of Sjögren's Disease using parotid gland ultrasonography. The code covers the entire pipeline from image preprocessing to model interpretability.

## 📂 Repository Structure

The notebooks are numbered to be run in sequential order:

* **`1-image-preprocessing.ipynb`**
    * Implements **Supplementary Algorithm S1**. Automatically crops the Parotid Gland Region of Interest (ROI) using adaptive projection profiles.
* **`2-dataset-split-sgkf.ipynb`**
    * Splits the dataset using **Stratified Group K-Fold (SGKF)** to ensure subject-level independence (preventing data leakage).
* **`3-model-training-ultralytics.ipynb`**
    * Training script for **YOLO11** variants (n/s/m/l) using the hyperparameters from the paper.
* **`3-model-training-pytorch.ipynb`**
    * Training script for comparison models (ResNet, DenseNet, EfficientNet).
* **`4-model-inference-ultralytics.ipynb`**
    * Runs inference on the test set and calculates metrics (Accuracy, Sensitivity, Specificity) found in **Table 4**.
* **`5.1-generate-cam-images.ipynb`** & **`5.2-generate-avg-cam-images.ipynb`**
    * Generates **Grad-CAM** visualizations (individual and averaged) for **Figures 3 & 4**.
* **`6-generate-roc-curve-image.ipynb`**
    * Plots the Receiver Operating Characteristic (ROC) curves for **Supplementary Figure S1**.

## ⚠️ Data Privacy
**Note:** The folder `data/` containing clinical ultrasound images is **not included** in this repository due to ethical and privacy restrictions. The code is provided to demonstrate the exact methodological pipeline used in the study.

## 🔗 Citation
(Citation details will be updated upon publication)