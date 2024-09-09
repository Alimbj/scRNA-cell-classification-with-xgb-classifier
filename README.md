# Brain Cell Type Classification Using scRNA-seq Data
Project Overview

This project focuses on classifying brain cell types using single-cell RNA sequencing (scRNA-seq) data. The primary objective is to build a machine learning model, specifically using XGBoost, to accurately identify cell types based on gene expression data. The data consists of gene expression counts and cell type annotations, which are used to train and evaluate the model.

Dataset

Source: The data can be downloaded from the Brain Image Library.
Files:
counts.h5ad: Contains normalized and preprocessed gene expression data with dimensions 280,186 cells × 254 genes. 
cell_labels.csv: Contains cell type annotations (3 classes).
Size: Approximately 1.0 GB.

Requirements

To run this project, the following dependencies are required:   
scanpy==1.10.0   
numpy==1.25.2   
pandas==2.1.1   
matplotlib==3.7.2   
seaborn==0.12.2   
scikit-learn==1.3.0   
xgboost==1.7.6   


Code Overview

The code is structured to follow these main steps:   
Data Loading and Preparation:     
Load the expression matrix (counts.h5ad) and cell type annotations (cell_labels.csv).    
Standardize the expression data using StandardScaler to ensure consistent input for the model.

Model Definition and Training:    
Define an XGBoost classifier with appropriate hyperparameters.    
Train the model on the standardized gene expression data.

Model Evaluation:    
Evaluate the model using accuracy, classification report, and confusion matrix to assess performance.
Perform cross-validation to ensure robust results.

Feature Importance:         
Plot the feature importances from the XGBoost model to identify which genes contribute most to the classification.

Download the required data files from https://download.brainimagelibrary.org/cf/1c/cf1c1a431ef8d021/processed_data/counts.h5ad

Key Results     
Accuracy: The model achieved an accuracy score of approximately 0.999 on the validation and test sets.    
Confusion Matrix: Visualizes the true vs. predicted cell types, highlighting the model’s strengths and weaknesses.     
Feature Importances: Highlights the most influential genes used by the XGBoost model for classification.     
