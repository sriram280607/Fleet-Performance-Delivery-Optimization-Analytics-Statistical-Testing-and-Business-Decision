
# Zomato Delivery Operations Analytics

## Project Overview
This project analyzes Zomato delivery data to understand delivery-time performance, examine traffic-related differences, and predict delivery duration using machine learning.

## Objectives
- Audit and clean the dataset.
- Calculate key delivery-time KPIs.
- Visualize delivery performance.
- Test differences in delivery time across traffic conditions.
- Compare a baseline model with a Random Forest regression model.
- Provide data-driven business recommendations.

## Dataset
- **Dataset:** Zomato Dataset.csv
- **Source:** Kaggle — dataset by saurabhbadole
- **Records:** 45,584
- **Columns:** 20
- **Date range:** 11 February 2022 – 6 April 2022
- **Target variable:** `Time_taken (min)`

## Tools Used
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- SciPy and Statsmodels
- Scikit-learn
- Google Colab / Jupyter Notebook

## Project Workflow
1. Dataset loading and inspection
2. Data quality audit and cleaning
3. KPI calculation
4. Exploratory data analysis and visualizations
5. One-way ANOVA and Tukey HSD testing
6. Baseline and Random Forest model evaluation
7. Feature importance analysis
8. Business recommendations

## Key Findings

### Delivery Performance
- Total orders: 45,584
- Average delivery time: 26.29 minutes
- Median delivery time: 26 minutes
- Orders taking more than 30 minutes: 13,602
- Percentage taking more than 30 minutes: 29.84%

### Traffic Analysis
- Jam traffic average: 31.18 minutes
- Low traffic average: 21.27 minutes
- Difference: approximately 9.91 minutes

ANOVA and Tukey HSD results indicate statistically significant differences between the traffic groups.

### Machine Learning Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Mean Baseline | 7.615 | 9.392 | 0.000 |
| Random Forest | 4.086 | 5.325 | 0.679 |

The Random Forest model performed better than the mean baseline on the test dataset.

### Important Features
- Delivery person ratings
- Delivery person age
- Multiple deliveries
- Road traffic density
- Vehicle condition
- Weather conditions

Feature importance indicates predictive contribution, not causation.

## Business Recommendations
- Account for traffic congestion when estimating delivery times.
- Review delivery batching and route assignments.
- Monitor delays under different weather conditions.
- Use machine learning predictions as estimates, not guarantees.
- Regularly evaluate model accuracy and data quality.

## Limitations
- The dataset covers a relatively short period.
- Statistical associations do not establish causation.
- Model performance may differ on future data.
- The selected Kaggle dataset differs from the transportation-data source recommended in the project brief.

## How to Run
1. Open `DA PROJECT.ipynb` in Google Colab or Jupyter Notebook.
2. Configure Kaggle access if required.
3. Install the required libraries.
4. Run notebook cells from top to bottom.
5. Review the generated tables, charts, statistical tests, and model results.

## Project Files
- `DA PROJECT.ipynb` — analysis notebook
- `DA_PROJECT.pdf` — PDF export
- `README.md` — project documentation

## Responsible Use
Predictions should support operational planning, not serve as the sole basis for evaluating delivery workers. Check data quality, fairness, and feature availability before deploying the model.
