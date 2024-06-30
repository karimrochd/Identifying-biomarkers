# Bio Informatics Project: ALS RNA Sequencing Analysis

## Students
- Karim Rochd
- Celina Bedjou


## Table of Contents
1. [Introduction](#introduction)
2. [Data Preprocessing](#data-preprocessing)
3. [Descriptive Analysis](#descriptive-analysis)
4. [Principal Component Analysis (PCA)](#principal-component-analysis-pca)
5. [tSNE and UMAP Analysis](#tsne-and-umap-analysis)
6. [Univariate Analysis](#univariate-analysis)
7. [Multivariate Analysis - Elastic-Net](#multivariate-analysis---elastic-net)
8. [XGBoost Analysis](#xgboost-analysis)
9. [Results Reporting](#results-reporting)

## Introduction
This project focuses on analyzing RNA sequencing data from Amyotrophic Lateral Sclerosis (ALS) patients. ALS is a severe neurodegenerative disease affecting motor neurons in the brain and spinal cord. Our goal is to discover distinctive molecular signatures associated with ALS, potentially aiding in understanding the disease's pathogenesis and developing new treatment strategies.

## Data Preprocessing
- **Data Source**: Post-mortem cerebral cortex biopsies from ALS patients and control subjects.
- **Data Format**: RNA count data in .txt files and annotations in XML format.
- **ALS_RNAseq Class**: Custom Python class for efficient data handling and analysis.
- **Preprocessing Steps**:
  - Loading RNA counts
  - Loading annotations
  - Data validation and integrity checks

## Descriptive Analysis
- **Sample Description**: Calculated mean, median, and standard deviation for each sample.
- **RNA Count Description**: Computed statistics for each gene, including percent difference between diseased and non-diseased samples.
- **Visualizations**:
  - Pie charts and bar graphs for sample distribution
  - Histograms for central tendency and dispersion measures
  - Summary tables for descriptive statistics

## Principal Component Analysis (PCA)
- **Data Standardization**: Used StandardScaler from sklearn.
- **Dimensionality Reduction**: Applied PCA to reduce data dimensions.
- **Visualization**: Plotted samples on planes formed by principal components.
- **Analysis**: Observed data structure, trends, and clustering between samples.

## tSNE and UMAP Analysis
- **Purpose**: To detect more complex groupings or separations in the data.
- **Visualization**: Projected samples onto reduced dimension space.
- **Analysis**: Examined structures and relationships between samples in the reduced space.

## Univariate Analysis
- **Data Preparation**: Synchronized count data with sample metadata.
- **DESeq2 Analysis**: 
  - Initialized DeseqDataSet
  - Performed differential expression analysis
- **Visualization**: Created volcano plot to represent statistical significance of expression changes.

## Multivariate Analysis - Elastic-Net
- **Purpose**: To identify genes most relevant in distinguishing ALS samples from healthy samples.
- **Method**: Used LogisticRegressionCV from scikit-learn with Elastic-Net regularization.
- **Evaluation**: Assessed model performance using ROC AUC.
- **Feature Importance**: Extracted and ranked model coefficients to identify important genes.

## XGBoost Analysis
- **Purpose**: To identify important genes for differentiating ALS samples from healthy samples.
- **Method**: Used XGBClassifier from XGBoost package.
- **Feature Importance**: Extracted and ranked feature importance from the model.
- **Evaluation**: Calculated accuracy and balanced accuracy on a validation set.

## Results Reporting
- **Objective**: Provide a list of 100 best candidate biomarkers for ALS and related neurological diseases.
- **Approach**:
  1. Differential expression analysis
  2. Elastic-Net feature selection
  3. XGBoost feature importance
- **Results**: Combined and normalized scores from all analyses to rank genes.
- **Output**: Top 100 candidate biomarkers saved in 'top_100_genes.csv'

