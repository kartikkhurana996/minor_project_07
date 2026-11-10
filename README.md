# QuickCart Warehouse Inventory Stockout Risk Prediction

## Project Overview

QuickCart is a machine learning project that predicts inventory stockout risk for different products across multiple stores.

The main objective is to classify inventory into three categories:

- **Safe:** Sufficient stock is available.
- **At-Risk:** Stock levels are getting low and require attention.
- **Imminent:** The product may run out of stock before the next supplier delivery.

This project uses historical inventory data, supplier information, store details, product characteristics, and festival events to predict stockout risk.

## Project Objectives

- Analyse daily inventory data.
- Combine multiple datasets using data merging techniques.
- Clean missing and inconsistent data.
- Perform Exploratory Data Analysis (EDA).
- Create meaningful features for machine learning.
- Build and evaluate classification models.
- Identify important factors influencing stockout risk.

## Dataset Description

The project uses five CSV files:

| File Name | Description |
|---|---|
| `dim_stores.csv` | Store information |
| `dim_skus.csv` | Product and SKU information |
| `dim_suppliers.csv` | Supplier information |
| `dim_events.csv` | Festival and promotional events |
| `fact_inventory_daily.csv` | Daily inventory records |

**Dataset size:** 21,600 inventory records.

**Dataset period:** 1 October 2026 – 30 October 2026.

**Stores:** 12  
**SKUs:** 60  
**Suppliers:** 15

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Project Workflow

### 1. Data Loading
Loaded all five CSV files into Python using Pandas.

### 2. Exploratory Data Analysis
Examined dataset structure, column information, missing values, duplicate records, and stockout-risk distribution.

### 3. Data Cleaning
- Standardised inconsistent city names.
- Converted supplier reliability scores into numeric values.
- Handled missing supplier reliability values.
- Checked and removed duplicate records.
- Converted date columns into datetime format.

### 4. Data Merging
Combined the five datasets using appropriate keys to create one master dataset.

### 5. Data Visualisation
Created visualisations to understand:
- Stockout-risk distribution.
- Festival impact on stockout risk.
- Supplier reliability and stockout risk.
- Perishable and non-perishable product risk.
- Daily stockout-risk trends.

### 6. Feature Engineering
Created additional features such as:

- `reorder_gap`
- `days_of_cover_ratio`
- `supplier_reliability_clean`
- `is_recent_reorder`
- `day_of_month`
- `days_since_festival_start`

Categorical variables were also converted into numerical features using one-hot encoding.

### 7. Train-Test Split
Used a time-based split:

- Training data: 1 October – 23 October 2026
- Testing data: 24 October – 30 October 2026

### 8. Machine Learning Models

Three classification models were implemented:

1. Majority Class Baseline
2. Logistic Regression
3. Random Forest Classifier

### 9. Model Evaluation
Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Special attention was given to recall for the Imminent class because missing a potential stockout is costly.

### 10. Feature Importance
Used Random Forest feature importance to identify the most influential features in the model's predictions.

## How to Run the Project

This project was developed using Google Colab.

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload the `QuickCart_Stockout_Analysis.ipynb` notebook.
3. Upload all five CSV files into the Colab session.
4. Execute the notebook cells in order.
5. Review the generated outputs, graphs, and model evaluation results.

## Expected Output

After executing the notebook, you will obtain:

- Cleaned and merged inventory dataset.
- Exploratory data analysis graphs.
- Feature-engineered dataset.
- Predictions from three machine learning models.
- Model performance comparison.
- Random Forest confusion matrix.
- Feature importance visualisation.
- Final business insights and conclusion.

## Business Insights

The project investigates how different operational factors influence stockout risk, including:

- Festival-related demand increases.
- Supplier reliability.
- Perishable product characteristics.
- Inventory and reorder levels.

These insights can help inventory teams plan replenishment, monitor high-risk products, and improve stock availability.

## Conclusion

The QuickCart Stockout Risk Prediction project demonstrates how machine learning can be applied to inventory management.

By combining multiple datasets, performing data cleaning, engineering features, and training classification models, the project aims to identify products that may run out of stock.

The resulting analysis can support better inventory planning, reduce stockout situations, and improve operational decision-making.

## Author

**Kartik Khurana**

B.Tech – Computer Science and Engineering

## Project Status

Completed – Data Analysis, Feature Engineering, Machine Learning Modelling, and Evaluation.
