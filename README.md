# Red Wine Quality Analysis Notebook

## Table of Contents

1.  [Introduction](#introduction)
2.  [Data Loading and Missing Value Handling](#data-loading-and-missing-value-handling)
3.  [Feature Selection and Covariance Matrix Calculation](#feature-selection-and-covariance-matrix-calculation)
4.  [Eigen Decomposition](#eigen-decomposition)
5.  [Vector Extraction](#vector-extraction)
6.  [Wine Quality Distribution Analysis](#wine-quality-distribution-analysis)

## 1. Introduction

This notebook performs an exploratory data analysis on the Red Wine Quality dataset. The primary goal is to understand the characteristics of different red wines and to identify key factors influencing their quality. This analysis includes data loading, handling missing values, feature engineering (covariance and eigen decomposition), and statistical analysis of wine quality distribution.

## 2. Data Loading and Missing Value Handling

The dataset, `winequality-red.csv`, was loaded into a Pandas DataFrame. An initial check for missing values was performed across all columns. It was found that the dataset is complete with no missing values, hence no imputation or removal of nulls was necessary.

## 3. Feature Selection and Covariance Matrix Calculation

Two key features, 'alcohol' and 'density', were selected for a detailed bivariate analysis. Their covariance matrix was calculated to understand the linear relationship and variability between these two properties. The covariance matrix provides insights into how these features vary together.

## 4. Eigen Decomposition

Eigen decomposition was performed on the calculated covariance matrix. This process yielded eigenvalues and eigenvectors:
*   **Eigenvalues:** Quantify the amount of variance explained by each principal component. The top eigenvalue indicates the direction of maximum variance.
*   **Eigenvectors:** Represent the principal components themselves, showing the directions in the feature space along which the data varies most. The top eigenvectors correspond to the largest eigenvalues.

These components are fundamental for dimensionality reduction techniques like Principal Component Analysis (PCA).

## 5. Vector Extraction

Specific columns, 'alcohol' and 'citric acid', were extracted as individual Pandas Series (vectors) from the main DataFrame. This step is useful for isolating and working with particular features for focused analysis or model input.

## 6. Wine Quality Distribution Analysis

The distribution of wine quality scores was analyzed to understand the prevalence of different quality ratings within the dataset. The analysis revealed that:
*   The most common wine quality score is **5**, with 681 occurrences.
*   This is closely followed by quality score **6**, with 638 occurrences.
*   The distribution is skewed towards average quality scores (5 and 6), with fewer wines receiving very low (3, 4) or very high (7, 8) ratings.

This suggests that the majority of red wines in this dataset fall within a moderate quality range, with extreme qualities being less common.
