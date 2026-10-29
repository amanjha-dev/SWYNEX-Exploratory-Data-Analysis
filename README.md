# SWYNEX – Exploratory Data Analysis (EDA)

## 1. Project Overview

This project performs Exploratory Data Analysis (EDA) on a cleaned retail dataset as part of my SWYNEX internship.

The objective is to understand sales and profit patterns, product category performance, regional differences, order statuses, customer satisfaction, returns, and potential data-quality issues.

## 2. Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Git and GitHub

## 3. Dataset Overview

- Total records: 4,200
- Total columns: 21
- Analysis period: January 2020 – December 2024
- Product categories: 7
- Regions: 5

The cleaned dataset from Task 1 was used for this analysis.

## 4. Analysis Performed

- Dataset structure and descriptive statistics
- Missing-value and duplicate checks
- Product category sales and profit analysis
- Regional sales and profit comparison
- Yearly and monthly sales trends
- Order-status distribution
- Customer satisfaction analysis
- Return-status analysis by product category
- Sales and profit anomaly investigation
- Comparison of recorded sales against calculated sales

## 5. Key Findings

1. **Category concentration:** Electronics contributes approximately 58.90% of recorded sales, while Furniture contributes approximately 21.46%. Together, they account for about 80.36% of recorded sales.

2. **Regional performance:** The South region has the highest recorded sales, approximately 27.82% of the total. The Central region has the lowest share at approximately 15.39%.

3. **Yearly trend:** Recorded sales peaked in 2023 at approximately 64.53 million. Sales declined by about 21.45% in 2024 compared with 2023.

4. **Order statuses:** Approximately 65.02% of records have a Delivered status. Returned and Cancelled records together account for approximately 22.81%.

5. **Customer satisfaction:** Average recorded customer satisfaction is approximately 3.02 out of 5, indicating scope for investigating customer experience.

6. **Return-status comparison:** Electronics has the highest status-based return percentage at approximately 15.79%, while Books has the lowest at approximately 13.52%.

7. **Sales data-quality issue:** Approximately 78.02% of records have a difference greater than 10% between recorded sales and sales calculated from quantity, unit price, and discount. The top 10 recorded sales values account for approximately 13.75% of total recorded sales.

## 6. Data Quality Limitations

The sales formula used for comparison was:

`quantity × unit_price × (1 − discount_pct)`

This formula does not match the recorded sales amount in 3,277 records when using a 10% difference threshold.

The original sales values were retained rather than overwritten. Consequently, sales and profit findings should be interpreted cautiously until the source of the inconsistencies is confirmed.

Customer satisfaction and shipping-time fields contain missing values. Missing customer satisfaction values were excluded from satisfaction summaries rather than imputed.

The return percentages represent the proportion of records with a Returned status within each category; they should not be interpreted as verified customer or product return rates without further information about the order lifecycle.

## 7. Repository Structure

```text
SWYNEX-Exploratory-Data-Analysis/
├── data/
│   └── cleaned_dataset.csv
├── notebooks/
│   └── exploratory_data_analysis.ipynb
├── charts/
├── README.md
├── requirements.txt
└── .gitignore
```

## 8. How to Run

1. Clone or download this repository.
2. Install the dependencies using `pip install -r requirements.txt`.
3. Open `notebooks/exploratory_data_analysis.ipynb` in Jupyter Notebook or VS Code.
4. Run the notebook cells in order.

## 9. Conclusion


This project demonstrates practical EDA using Python, including descriptive statistics, grouping and aggregation, trend analysis, visualization, and data-quality validation.

The analysis identifies useful patterns across categories, regions, order statuses, and customer satisfaction while highlighting the importance of validating financial data before making business decisions.

## 10. Acknowledgement

Completed as part of the SWYNEX internship.

