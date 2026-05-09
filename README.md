# Machine-Learning-Assignment 1


🏠 House Prices Prediction - Data Preprocessing (EDA & Feature Engineering)

📌 Project Overview (Problem Description)

This project focuses on analyzing and preprocessing a real-world dataset .

The main goal is to apply full Data Preprocessing and Feature Engineering steps to prepare the dataset for a future Machine Learning regression model that predicts house prices (SalePrice).



📊 Dataset Description

The project uses two main files:

train.csv → Training dataset containing the target variable SalePrice

test.csv → Test dataset without the target variable


The dataset includes approximately 79 features describing different aspects of residential houses in Ames, Iowa, such as:

Building characteristics

Area measurements

Quality ratings

Location (Neighborhood)

Other property attributes


🔍 Workflow Steps

1. Data Loading & Inspection

Load datasets using Pandas

Check dataset shape

Display first 5 rows

Analyze data types for memory optimization


2. Data Cleaning

Handling Missing Values:

Features like PoolQC, Fence, and Alley were treated as meaningful categories (e.g., "No Pool")

Other missing values were filled using appropriate strategies (median or categorical filling)


Outlier Detection:

Distribution of SalePrice was analyzed

Extreme values (especially in GrLivArea) were identified

Decisions were made whether to remove or keep outliers based on their impact


Target Transformation:

Applied logarithmic transformation using:

np.log1p() to normalize the skewed distribution of SalePrice



3. Exploratory Data Analysis (EDA)

Built a Correlation Matrix

Used a heatmap to identify features most correlated with SalePrice

Extracted the top 5 most important features

Scatter Plot Analysis:

Relationship between GrLivArea and SalePrice

Colored by OverallQual


Geographical Insights:

Average SalePrice per Neighborhood

Visualized using Seaborn / Plotly


4. Feature Engineering

Created a new feature:

TotalSF = TotalBsmtSF + 1stFlrSF + 2ndFlrSF


Encoding Categorical Variables:

Label Encoding for ordinal features:

Example: ExterQual, KitchenQual


One-Hot Encoding for nominal features:

Example: Neighborhood, BldgType



5. Pipeline Construction

A reusable function / pipeline was created to ensure:

Consistent preprocessing for both training and test datasets

Automated cleaning, transformation, and encoding steps


📈 Key Findings

The most influential features affecting house prices are:

Overall quality (OverallQual)

Living area size (GrLivArea)

Total square footage (TotalSF)


Location (Neighborhood) has a strong impact on house prices

The target variable (SalePrice) was highly skewed and improved after log transformation


▶️ How to Run the Project

📌 On Google Colab:

1. Open the notebook file


2. Upload:

train.csv

test.csv



3. Run all cells from top to bottom

