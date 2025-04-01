# Indian Traffic Violations Analysis Project

## Project Overview

This project analyzes the "Indian_Traffic_Violations.csv" dataset to gain insights into traffic violations, fine amounts, and related factors. The analysis aims to understand patterns, identify trends, and provide actionable information related to traffic violations in the region.

## Project Goals

* Load and explore the traffic violations dataset.
* Clean the data by handling missing values, inconsistencies, and outliers.
* Wrangle the data to prepare it for analysis and visualization.
* Perform exploratory data analysis (EDA) to understand feature distributions and relationships.
* Visualize key findings to communicate insights effectively.
* Prepare the data for question answering and knowledge base construction.

## Methodology

This project follows a structured data analysis pipeline:

1.  **Data Loading:**
    * Loading the "Indian_Traffic_Violations.csv" file into a Pandas DataFrame.

2.  **Data Exploration:**
    * Examining data types, missing values, descriptive statistics, and value counts for categorical variables.
    * Identifying potential issues like inconsistencies or outliers.
    * Determining the overall size and shape of the data.

3.  **Data Cleaning:**
    * Imputing missing values in 'Helmet_Worn', 'Seatbelt_Worn', and 'Comments'.
    * Converting the 'Date' column to datetime and removing invalid (future) dates.
    * Converting the 'Violation_ID' column to integer type.
    * Addressing inconsistencies in categorical columns.

4.  **Data Wrangling:**
    * Combining 'Date' and 'Time' columns into a 'Violation_Datetime' column.
    * Grouping similar violation types into broader categories.
    * Creating binary features (e.g., 'Seatbelt_Worn_Binary').
    * Creating a 'Vehicle_Age' numerical feature.
    * One-hot encoding categorical features.

5.  **Data Analysis:**
    * Calculating descriptive statistics for numerical features.
    * Generating a correlation matrix to examine relationships between numerical variables.
    * Visualizing distributions of numerical and categorical features.
    * Performing group-wise analysis (e.g., mean fines by violation category).

6.  **Data Visualization:**
    * Creating histograms for numerical feature distributions.
    * Generating scatter plots for numerical feature relationships.
    * Producing bar charts for categorical feature distributions.
    * Creating a heatmap of the correlation matrix.
    * Generating box plots to show 'Fine_Amount' distribution across violation categories.

7.  **Data Preparation for Question Answering:**
    * Creating a knowledge base by grouping data for faster query answering.
    * Generating new DataFrames for aggregations and summaries based on violation types, locations, and time periods.

## Key Findings

* **Missing Data Imputation:**
    * Missing values were handled by imputing with mode for 'Helmet_Worn' and 'Seatbelt_Worn' and "No Comment" for 'Comments'.
* **Data Type Correction:**
    * The 'Date' column was converted to datetime, and invalid dates were removed.
    * The 'Violation_ID' column was converted to integer.
* **Outlier Handling:**
    * Future dates in the 'Date' column were identified and removed.
* **Feature Engineering:**
    * New features like 'Violation_Datetime', 'Violation_Category', 'Seatbelt_Worn_Binary', and 'Vehicle_Age' were created.
    * One-hot encoding resulted in 82 columns in the final DataFrame.
* **Correlation Analysis:**
    * A correlation matrix was generated for numerical features.
* **Group-wise Analysis:**
    * Mean and standard deviation of 'Fine_Amount' were calculated and visualized for groups based on violation categories and registration states.

## Example Q&A

* **Q:** What is the average fine for speeding violations?
    * **A:** The average fine for speeding violations is 1078.02.
* **Q:** What is the total fine amount collected from speeding violations?
    * **A:** The total fines collected from speeding violations is 1,265,345.

## Tools Used

* Python
* Pandas
* NumPy
* Seaborn
* Matplotlib
