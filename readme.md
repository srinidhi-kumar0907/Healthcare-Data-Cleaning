# Healthcare Data Cleaning & Preprocessing
## 1. Project Overview

This project focuses on cleaning and preprocessing a messy, real-world healthcare dataset using Python and Pandas. The dataset contains more than 10,000 records with missing values, duplicate records, inconsistent data types, and other data-quality issues.
The main objective is to transform the raw dataset into a clean, consistent, and analysis-ready dataset.

## 2. Objectives
* Load and inspect the raw healthcare dataset.
* Identify missing values.
* Handle missing and inconsistent data.
* Detect and remove duplicate records.
* Correct incorrect data types.
* Identify and handle outliers.
* Standardize inconsistent values.
* Generate a cleaned dataset for further analysis.
* Compare the dataset before and after cleaning.

## 3. Technologies Used
* Python
* Pandas – Data loading, cleaning, and preprocessing
* Jupyter Notebook– Implementation and documentation

## 4. Dataset
The project uses a healthcare dataset containing patient/medical-related records.
The raw dataset may contain:
* Missing values
* Duplicate records
* Incorrect data types
* Inconsistent categorical values
* Invalid or unusual numerical values
* Outliers
The raw data is stored in the data folder.
## 5. Data Cleaning Process
### Step 1: Load the Dataset
The raw dataset is loaded into a Pandas DataFrame using `pd.read_csv()`.
### Step 2: Initial Data Inspection
The dataset is inspected using:
* `head()`
* `tail()`
* `info()`
* `describe()`
* `shape`
* `dtypes`
This helps understand the structure and quality of the dataset.
### Step 3: Missing Value Handling
Missing values are identified using:
```python
df.isnull().sum()
```
Appropriate methods are used to handle missing values, such as:
* Replacing missing numerical values with suitable statistical values.
* Replacing missing categorical values with the mode or an appropriate category.
* Removing records only when necessary.
### Step 4: Duplicate Removal
Duplicate records are identified using:
```python
df.duplicated().sum()
```
Duplicate rows are removed to prevent repeated records from affecting analysis.
### Step 5: Data Type Correction
Incorrect data types are identified and converted into appropriate formats.
Examples include:
* Converting numerical columns to numeric data types.
* Converting date columns to datetime format.
* Converting categorical columns to appropriate types where required.
### Step 6: Inconsistent Data Handling
Inconsistent values are standardized to maintain uniformity throughout the dataset.
Examples include:
* Different spellings of the same category.
* Extra spaces.
* Different capitalization.
* Invalid categorical values.
### Step 7: Outlier Detection
Numerical columns are examined for unusual values using statistical techniques such as the Interquartile Range (IQR).
Outliers are reviewed and handled appropriately without unnecessarily removing valid healthcare records.
### Step 8: Final Validation
After cleaning, the dataset is checked again for:
* Remaining missing values
* Duplicate records
* Incorrect data types
* Invalid values
* Data consistency
The final dataset is then saved in the `output` folder.

## 6. Project Structure
Healthcare-Data-Cleaning/
│
├── data/
│   └── raw_dataset.csv
│
├── output/
│   └── cleaned_dataset.csv
│
├── Healthcare_Data_Cleaning.ipynb
│
└── README.md

## 7. Input and Output
### Input
The raw and uncleaned healthcare dataset is stored in the `data` folder.
### Output
The cleaned and processed dataset is stored in the `output` folder.
The output dataset is suitable for further data analysis and machine learning applications.

## 8. Results
After preprocessing:
* Duplicate records were identified and handled.
* Missing values were analyzed and handled.
* Incorrect data types were corrected.
* Inconsistent values were standardized.
* Outliers were identified and appropriately handled.
* The final dataset was validated and exported.
* 
## 9. How to Run the Project
1. Install Python.
2. Install the required libraries:
pip install pandas numpy matplotlib jupyter
3. Open Jupyter Notebook:
jupyter notebook
4. Open `Healthcare_Data_Cleaning.ipynb`.
5. Run the notebook cells from beginning to end.
6. The cleaned dataset will be generated in the `output` folder.
7. 
## 10. Conclusion
This project demonstrates the complete data cleaning and preprocessing workflow using Pandas. By identifying and handling missing values, duplicates, incorrect data types, inconsistencies, and outliers, the raw healthcare dataset was transformed into a cleaner and more reliable dataset.
The cleaned data can be used for further exploratory data analysis, visualization, statistical analysis, and machine learning applications.
