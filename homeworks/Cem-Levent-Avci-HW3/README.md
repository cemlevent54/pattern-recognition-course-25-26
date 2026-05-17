
# Radiomics Classification Notebook

## Overview

This Google Colab notebook demonstrates a complete workflow for radiomics-based classification of chest CT-scan images. The process includes:

1.  **Dataset Preparation:** Downloading the Chest CT-Scan Images dataset from Kaggle.
2.  **Data Preprocessing:** Loading, resizing, converting to grayscale, creating binary masks using Otsu thresholding, and encoding labels.
3.  **Radiomic Feature Extraction:** Extracting a comprehensive set of radiomic features using the PyRadiomics library.
4.  **Feature Selection:** Reducing dimensionality and improving model performance through variance thresholding, standardization, correlation filtering, and supervised feature selection (SelectKBest).
5.  **Model Training and Hyperparameter Optimization:** Training and optimizing Random Forest and K-Nearest Neighbors (KNN) classifiers.
6.  **Model Evaluation and Visualization:** Comprehensive evaluation of model performance using various metrics and visualizations like confusion matrices and feature importance plots.

## Setup Instructions

To run this notebook successfully, please follow these steps:

1.  **Create a Google Drive Folder:**
    In your Google Drive, create a folder named `pr_hw3_152120211071` directly under "My Drive". The full path should be `/content/drive/MyDrive/pr_hw3_152120211071/`.

2.  **Obtain Kaggle API Key:**
    *   Go to Kaggle (www.kaggle.com), log in, and navigate to your account settings.
    *   Under the "API" section, click "Create New API Token" to download `kaggle.json`.

3.  **Place `kaggle.json` in Google Drive:**
    Upload the `kaggle.json` file you just downloaded into the `pr_hw3_152120211071` folder you created in Step 1. The file path should be `/content/drive/MyDrive/pr_hw3_152120211071/kaggle.json`.

4.  **Open the Notebook in Google Colab:**
    Upload and open this notebook in Google Colab.

## Running the Notebook

1.  **Mount Google Drive:**
    The notebook will likely prompt you to mount your Google Drive. Follow the instructions to allow Colab to access your Drive files. This is typically done by running a cell with `from google.colab import drive; drive.mount('/content/drive')`.

2.  **Execute Cells Sequentially:**
    Run all cells in the notebook from top to bottom. The notebook is designed to be executed linearly.

3.  **Radiomic Feature Extraction Control:**
    *   There is a flag `LOAD_PRE_EXISTING_RADIOMICS_FEATURES` in the notebook (in section "3. Radiomic Feature Extraction").
    *   Set `LOAD_PRE_EXISTING_RADIOMICS_FEATURES = False` to re-extract features (this is the default and recommended for the first run).
    *   Set `LOAD_PRE_EXISTING_RADIOMICS_FEATURES = True` to load features from previously saved CSV files (if they exist in the `radiomics_features` folder within your Google Drive). This can save time on subsequent runs.

## Dataset Information

The dataset used in this notebook is:

*   **Title:** Chest CT-Scan Images
*   **Author:** Mohamed Hany
*   **URL:** https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images
*   **License:** CC BY-NC-SA 4.0

This dataset contains chest CT-scan images categorized into four classes: adenocarcinoma, large cell carcinoma, squamous cell carcinoma, and normal.

