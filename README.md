# ML-Data-Cleaning

##  Project Title
**Robust Data Preprocessing for Real-World Datasets**


##  Objective

This project demonstrates the design and implementation of a comprehensive data preprocessing pipeline for cleaning, validating, and preparing employee data for machine learning. The preprocessing steps focus on:
- Handling missing values  
- Removing outliers  
- Correcting inconsistent formatting  
- Encoding categorical features  
- Feature scaling for model readiness  

##  Files in the Repository

| File Name                | Description                                   |
|-------------------------|-----------------------------------------------|
| `Employee.csv`          | Raw input dataset with missing/inconsistent values |
| `cleaned_data.csv`      | Cleaned and processed dataset, ready for ML   |
| `ML Data cleaning.py`   | Python script for data preprocessing steps    |


##  Dataset Overview

The dataset (`Employee.csv`) includes fictional employee records with the following columns:

- `Company` – Name of the organization  
- `Age` – Employee’s age (some values are 0 or missing)  
- `Salary` – Monthly salary in INR  
- `Place` – City of employment  
- `Country` – Country (all entries = India)  
- `Gender` – Encoded: 0 = Male, 1 = Female  


##  Technologies Used

- Python 3  
- Pandas  
- NumPy  
- Seaborn / Matplotlib  
- Jupyter Notebook  


##  Project Workflow

### 1.  Data Exploration
- Loaded data from `Employee.csv`
- Renamed columns for consistency
- Displayed unique values for each column
- Summarized data using `.describe()` and `.info()`

### 2. Data Cleaning
- Replaced `0` values in `Age` with `NaN`
- Converted `Gender` values from numeric to text (`Male` / `Female`)
- Identified and treated missing values using:
  - Mode (for categorical variables)
  - Median (for numeric columns)
- Removed duplicate rows

### 3. Outlier Detection
- Used the **IQR (Interquartile Range)** method on the `Salary` column
- Printed detected outlier rows for review

### 4.  Data Analysis
- Filtered employees where `Age > 40` and `Salary < 5000`
- Counted the number of employees per city
- Visualized relationships using:
  - Bar charts (`Place` distribution)
  - Scatter plots (`Age` vs `Salary`)

### 5.  Encoding Categorical Data
- Applied:
  - **Label Encoding** (for ordinal categories)
  - **One-Hot Encoding** (for nominal variables)

### 6.  Feature Scaling
- Applied both:
  - **StandardScaler**
  - **MinMaxScaler**
- Output saved as `cleaned_data.csv`


## Output

- Final dataset: `cleaned_data.csv`
- All missing values handled
- Outliers either removed or capped
- All columns properly encoded
- Features scaled for model training
