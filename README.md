# 21CSE321T Data Warehousing and Data Mining - Assignment 2

This repository contains the complete implementation of **Assignment 2** for the course **21CSE321T: Data Warehousing and Data Mining**, executed using the **Orange Data Mining** visual workflow platform.

---

## 📁 Repository Structure

```text
├── datasets/          # Data files used for experiments (.csv, .tab)
├── output/            # Result screenshots for all 9 tasks (.png)
├── workflows/         # Orange workflow canvas files (.ows)
└── README.md          # Assignment documentation

```

---

## 📋 Experiments & Task Summary

| Task # | Experiment Description

 | Key Widgets / Algorithm Used | Output File Location |
| --- | --- | --- | --- |
| **1** | Data Cleaning on Dataset

 | `File` $\rightarrow$ `Impute` $\rightarrow$ `Data Table`

 | `output/` (Data Cleaning screenshot)

 |
| **2** | Data Reduction on Dataset

 | `File` $\rightarrow$ `PCA` $\rightarrow$ `Data Table`

 | `output/` (PCA Variance plot/table)

 |
| **3** | Data Transformation

 | `File` $\rightarrow$ `Preprocess` (Normalize) $\rightarrow$ `Data Table`

 | `output/` (Normalized Data Table)

 |
| **4** | Association Rules via Apriori Algorithm

 | `File` $\rightarrow$ `Association Rules` (Apriori)

 | `output/` (Apriori Rules table)

 |
| **5** | Statistical Analysis on Dataset

 | `Column Statistics`, `Box Plot`

 | `output/` (Summary stats & Box plot)

 |
| **6** | Regression Performance Demonstration

 | `Select Columns` $\rightarrow$ `Linear Regression` $\rightarrow$ `Test & Score`

 | `output/` (Regression evaluation metrics)

 |
| **7** | Implementation of Outlier Analysis

 | `Outliers` (Isolation Forest) $\rightarrow$ `Scatter Plot`

 | `output/` (Colored Outlier Scatter Plot)

 |
| **8** | K-Means Algorithm for Iris Dataset

 | `File` (Iris) $\rightarrow$ `k-Means` $\rightarrow$ `Scatter Plot`, `Silhouette Plot`

 | `output/` (Cluster Scatter Plot & Silhouette Plot)

 |
| **9** | Clustering Rule Process on Iris Dataset

 | `k-Means` $\rightarrow$ `Tree` $\rightarrow$ `Tree Viewer`

 | `output/` (Decision Tree Viewer diagram)

 |

---

## 🛠️ Detailed Overview of Tasks

### Task 1: Data Cleaning

Demonstrates handling missing values (represented by `?` symbols) in datasets using the **Impute** widget with average/mode imputation and instance filtering.

### Task 2: Data Reduction

Applies **Principal Component Analysis (PCA)** to reduce multi-dimensional continuous datasets down to principal components while retaining maximum cumulative variance.

### Task 3: Data Transformation

Performs feature standardization ($\mu = 0, \sigma = 1$) and continuous variable discretization via the **Preprocess** widget.

### Task 4: Association Rule Generation

Derives frequent itemsets and association rules ($A \implies B$) using the **Apriori algorithm** from the Orange Associate extension, evaluated on Support, Confidence, and Lift metrics.

### Task 5: Statistical Analysis

Generates descriptive summary statistics (mean, mode, median, dispersion, min/max, distribution histograms) and quartile visualizations using **Column Statistics** and **Box Plot** widgets.

### Task 6: Linear Regression Analysis

Configures continuous target variables via **Select Columns** and evaluates Linear Regression predictive model accuracy ($MSE$, $RMSE$, $MAE$, $R^2$) using cross-validation inside **Test & Score**.

### Task 7: Outlier Analysis

Implements anomaly detection using **Isolation Forest** algorithms to detect outlier instances and visualize them across scatter plots.

### Task 8: K-Means Clustering on Iris Dataset

Applies unsupervised **$k$-Means clustering** ($k = 3$) on the benchmark Iris dataset, verified using multi-cluster **Scatter Plots** and **Silhouette Plots**.

### Task 9: Clustering Rule Extraction

Feeds $k$-Means cluster outputs into a **Tree** classifier to extract readable decision rules explaining cluster boundaries within the **Tree Viewer**.

---

## 🚀 How to Run the Workflows

1. Install **[Orange Data Mining](https://orangedatamining.com/)**.
2. Install the **Orange3-Associate** add-on via `Options` > `Add-ons...` in Orange (required for Task 4).
3. Open Orange, navigate to `File` > `Open`, and select `workflows/one.ows`.


4. Double-click any output widget (e.g., `Data Table`, `Test & Score`, `Scatter Plot`, `Tree Viewer`) to inspect results.
