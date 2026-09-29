# Customer Segmentation using Unsupervised Learning

Segmenting customers into groups with similar demographics and purchasing behavior using PCA, K-Means, and Agglomerative Clustering.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Workflow](#workflow)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)

## Overview

The objective is to analyze customer demographic and purchasing behavior and identify meaningful groups of customers with similar characteristics. The project covers data preprocessing, feature engineering, exploratory data analysis, dimensionality reduction, and clustering.

## Dataset

- **Source:** Marketing Campaign dataset
- **Size:** 2,240 customers, 29 features
- **Contents:** demographics, income, household information, purchase behavior, campaign responses, recency, and spending across product categories

## Workflow

### 1. Data Preprocessing
- Handled missing values
- Processed categorical variables
- Removed features not required for clustering
- Standardized numerical features using `StandardScaler`

### 2. Feature Engineering
Features derived from the existing data:

| Feature | Description |
|---|---|
| Age | Customer age |
| Total spending | Combined spending across product categories |
| Number of children | Children in the household |
| Family size | Total household size |
| Living situation | Household living arrangement |
| Customer tenure | Duration as a customer |
| Parent status | Whether the customer is a parent |

### 3. Exploratory Data Analysis
- Pair plots and other visualizations of income, recency, customer tenure, age, spending, and parent status
- Identification of unusual observations and potential outliers

### 4. Dimensionality Reduction
- Applied Principal Component Analysis (PCA) to reduce dimensionality while retaining the information needed for clustering
- Used the principal components to visualize customers in a lower-dimensional space

### 5. Clustering
- **K-Means:** number of clusters evaluated with the Elbow Method
- **Agglomerative Clustering:** hierarchical approach used for comparison

## Technologies Used

| Purpose | Libraries |
|---|---|
| Data processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Preprocessing, PCA, clustering | Scikit-learn |
| Cluster evaluation | Yellowbrick |

## Project Structure

```text
customer-segmentation/
├── customer_segmentation.ipynb
└── README.md
```

## Getting Started

1. Install the dependencies:
```bash
   pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick
```
2. Open `customer_segmentation.ipynb` in Jupyter Notebook or JupyterLab.
3. Run the cells in order.
