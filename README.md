# Data Quality Report and Exploratory Data Analysis with ydata-profiling

## Project Overview

This project demonstrates the use of `ydata-profiling` (formerly `pandas-profiling`) to generate a comprehensive **Exploratory Data Analysis (EDA) report** and assess data quality for a given dataset. The primary goal is to quickly understand the structure, characteristics, and potential issues within the data without writing extensive manual plotting or descriptive code.

By automating the generation of a detailed HTML report, this project highlights key aspects of data quality, including missing values, unique values, data types, distributions, and correlations, enabling a rapid initial assessment for further analysis or machine learning tasks.

## Dataset Used

The project utilizes the **Titanic dataset** (from `train.csv`), a classic dataset in data science often used for classification tasks. It contains information about passengers on the Titanic, including survival status, class, age, gender, and more.

## Key Activities

The core of this project involves leveraging the `ydata-profiling` library to automatically generate a rich HTML report:

### 1. Data Loading

* The Titanic dataset (`train.csv`) was loaded into a Pandas DataFrame for initial inspection.
    * **Example:** Viewing the first few rows (`df.head()`) to understand the columns and their data types.
    * **Example:** Generating basic descriptive statistics (`df.describe()`) for numerical columns to get quick summaries like mean, min, max, and quartiles.

### 2. Profile Report Generation

* The `ProfileReport` function from `ydata-profiling` was used on the loaded DataFrame. This function automatically analyzes every column in the dataset and generates a detailed interactive report.
* The generated report was then saved as an `output.html` file, which can be opened in any web browser.

### 3. Insights Provided by the Report

The `ydata-profiling` report offers a wealth of information at a glance, typically including:

* **Overview:** Number of variables, observations, missing cells, duplicate rows, memory size.
* **Variable Types:** Automatic detection and classification of data types (numerical, categorical, boolean, date, etc.).
* **Missing Values:** Detailed breakdown of missing data per column, including visual representations (bar chart, matrix).
* **Descriptive Statistics:** For numerical variables: mean, median, mode, standard deviation, variance, skewness, kurtosis, quartiles, range, interquartile range (IQR).
* **Histograms/Distributions:** Visualizations of the distribution of values for each variable.
* **Categorical Value Counts:** Frequency tables and bar charts for categorical variables.
* **Correlations:** Heatmaps showing Pearson, Spearman, Kendall, and Phik correlations between variables, helping identify strong relationships.
* **Interactions:** Scatter plots for numerical variable pairs to visualize relationships.
* **Duplicate Rows:** Identification of completely duplicate rows in the dataset.

This automated reporting significantly streamlines the initial phases of data understanding and quality assessment.

## Technologies Used

* **Python:** The core programming language used.
* **Pandas:** For data manipulation and loading the dataset.
* **ydata-profiling (formerly pandas-profiling):** The primary library used for generating the comprehensive data quality report.
