# Analyzing Used Car Prices

This project explores a dataset of used cars to understand the factors that influence their price. The analysis follows the CRISP-DM framework, starting from understanding the business problem to data preparation and initial modeling.

## Project Goal

The primary goal is to identify key drivers for used car prices and provide insights to a used car dealership on what consumers value in a used car.

## Dataset

The dataset used is a subset of a larger Kaggle dataset, containing information on approximately 426K used cars.

## CRISP-DM Framework

The project is structured around the CRISP-DM methodology:

1.  **Business Understanding:** Reframing the business problem of identifying price drivers into a data task.
2.  **Data Understanding:** Exploring the dataset to understand its structure, content, and potential quality issues.
3.  **Data Preparation:** Cleaning the data, handling missing values, removing outliers, and preparing the data for modeling. This involves:
    *   Dropping irrelevant columns.
    *   Handling missing values in various columns.
    *   Filtering out extreme price and odometer values.
    *   Separating premium and electric cars for potentially separate analysis.
    *   Filtering specific car types and manufacturers.
    *   Removing cars older than 2000.
    *   Focusing on 'gas' fuel type cars.
    *   Exploring average prices by year, transmission, drive type, and title status.
4.  **Modeling:** Building various regression models to predict car prices based on different feature sets.
5.  **Evaluation:** (To be added)
6.  **Deployment:** (To be added)

## Analysis Highlights

*   Initial correlation analysis on a popular car model showed a positive correlation between year and price, and a negative correlation between odometer and price.
*   Data cleaning involved addressing missing values and removing potential outliers in price and odometer readings.
*   Exploratory analysis on subsets of the data (e.g., by transmission, drive type, title status) revealed potential relationships with price.
*   Initial linear regression models were built using:
    *   Odometer as a predictor.
    *   Odometer and year as predictors.
    *   Odometer, year, and one-hot encoded title status as predictors.
*   K-Means clustering was applied to group cars based on numerical features like price, odometer, and year, providing initial insights into car segmentation.

## Notebook Contents

The notebook contains the following sections:

*   **Business Understanding:** Defining the data task.
*   **Data Understanding:** Steps taken to explore the dataset and identify quality issues.
*   **Data Preparation:** Detailed steps for cleaning, filtering, and preparing the data. This includes:
    *   Loading the data.
    *   Handling missing values.
    *   Dropping rows based on price and odometer.
    *   Creating subsets for premium and electric cars.
    *   Filtering by car type and manufacturer.
    *   Analyzing average prices by various categories.
*   **Modeling:** Building and evaluating initial regression models.
    *   Linear Regression with Odometer.
    *   Multiple Linear Regression with Odometer and Year.
    *   Multiple Linear Regression with Odometer, Year, and Title Status.
    *   K-Means Clustering for car segmentation.

## Getting Started

To run this notebook:

1.  Open the notebook in Google Colab.
2.  Ensure the `data/vehicles.csv` file is accessible in your Colab environment (e.g., by uploading it or mounting your Google Drive).
3.  Run the code cells sequentially.

## Dependencies

The notebook uses the following libraries:

*   `pandas`
*   `numpy`
*   `matplotlib`
*   `seaborn`
*   `sklearn`

These libraries are typically pre-installed in Google Colab.

## Future Work

*   Further feature engineering.
*   Exploring more advanced regression models (e.g., Ridge, Lasso, Polynomial Regression, tree-based models).
*   Hyperparameter tuning and cross-validation.
*   Comprehensive model evaluation using various metrics.
*   Analyzing the premium and electric car subsets.
*   Providing clear recommendations based on the analysis findings.
