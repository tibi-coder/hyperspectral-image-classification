# Hyperspectral Image Classification

This project implements a deep learning pipeline for hyperspectral image classification developed for the Kaggle competition:

Hyperspectral Image Classification
https://www.kaggle.com/competitions/hsi-classification

## Project Overview

Hyperspectral images capture information across dozens of spectral bands for each pixel, providing detailed data about the physical properties of materials. Unlike standard RGB images, hyperspectral data allows models to distinguish between surfaces or materials that appear visually similar but differ spectrally.

The objective of this project is to classify hyperspectral image samples into several land-cover categories by leveraging both spectral and spatial information contained in the data.

## Approach

The proposed solution uses a spectral–spatial neural network architecture that combines 3D and 2D convolutional layers.

First, 3D convolutions are used to extract joint spectral–spatial features from the hyperspectral cube. These layers capture correlations across spectral bands while preserving spatial context. The resulting representations are then reshaped and processed by 2D convolutional layers that further refine spatial features before the final classification stage.

To improve generalization and model robustness, the training pipeline incorporates several techniques:

* stratified k-fold cross validation
* normalization of hyperspectral data
* spatial data augmentation through rotations and flips
* test-time augmentation during inference
* probability calibration to address class imbalance

These techniques help stabilize training and improve predictive performance on unseen data.

## Competition Context

This work was developed as part of the *Hyperspectral Image Classification* Kaggle competition, where participants were tasked with building models capable of accurately classifying hyperspectral image samples based on their spectral signatures.

The challenge highlights the complexity of working with high-dimensional spectral data and requires models that can effectively combine spectral and spatial information.

## Author
George-Tiberiu Samoila

Kaggle: tibisamoila
