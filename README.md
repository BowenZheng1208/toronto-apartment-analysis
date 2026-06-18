# 🏢 Toronto Apartment Building Analysis

## Overview

This project explores apartment building evaluation data from **Toronto Open Data** to investigate how building characteristics, maintenance conditions, and ownership types influence overall building evaluation scores.

The project combines **exploratory data analysis, clustering, regression modeling, feature extraction, dimension reduction, and data visualization** into a reproducible R Markdown workflow.

---

## Dataset

**Source**

Toronto Open Data – Apartment Building Evaluations Dataset

The dataset contains information on apartment buildings including:

* Building age
* Number of storeys
* Number of units
* Security condition
* Stairwell condition
* Interior lighting
* Graffiti condition
* Property type
* Geographic location

More than **9,500 apartment buildings** were included in the final analysis after data cleaning.

---

## Project Workflow

### 1. Data Cleaning

* Standardized variable names
* Selected relevant features
* Converted variables into appropriate formats
* Created derived variable:

  * Building Age = Year Evaluated − Year Built
* Removed missing observations

---

### 2. Exploratory Data Analysis

Performed:

* Summary statistics
* GGPairs visualization
* Correlation analysis
* Distribution visualization

Key findings:

* Building age is negatively associated with evaluation score.
* Security condition is positively associated with evaluation score.
* Storeys and units show strong positive correlation.

---

### 3. K-Means Clustering

Applied K-Means clustering to identify apartment building profiles.

Features include:

* Security
* Stairwells
* Interior lighting
* Graffiti
* Entrance condition
* Parking area
* Building size

The elbow method suggested a **4-cluster solution**, representing different maintenance and building-size profiles.

---

### 4. Multiple Linear Regression

Response variable:

* Building Evaluation Score

Predictors:

* Building age
* Log(storeys)
* Log(units)
* Security
* Stairwells
* Interior lighting
* Graffiti
* Property type

Model performance:

* **R² ≈ 0.79**

Major findings:

* Better maintenance conditions significantly improve evaluation scores.
* Older buildings tend to receive lower scores.

---

### 5. Random Forest Feature Extraction

Random Forest was used to evaluate predictor importance.

Important variables include:

* Parking area
* Security
* Entrance doors/windows
* Stairwells
* Interior lighting

The model explained approximately **89.7% of score variance**.

---

### 6. Principal Component Analysis (PCA)

PCA was applied to summarize correlated condition variables.

Results:

* PC1 explains approximately **48.5%** of total variance.
* The first three principal components explain approximately **71.7%** of total variance.

---

### 7. Data Visualization

The project includes multiple visualization techniques:

* GGPairs plot
* Elbow plot
* Cluster visualization
* Random Forest variable importance
* PCA scree plot
* PCA loading plot
* Toronto ward choropleth map
* Apartment profile heatmap

---

## Tech Stack

* R
* tidyverse
* GGally
* factoextra
* randomForest
* sf
* janitor
* broom
* ggplot2

---

## Repository Structure

```
.
├── README.md
├── opentoronto.Rmd
└── opentoronto.pdf
```

---

## Key Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Feature Engineering
* K-Means Clustering
* Multiple Linear Regression
* Random Forest
* Principal Component Analysis (PCA)
* Data Visualization
* Reproducible Research with R Markdown

---

## Author

**Bowen Zheng**

Master of Data Science and Artificial Intelligence

University of Waterloo
