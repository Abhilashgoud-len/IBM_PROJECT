# AI Predicts What Happens Next: Customer Churn Prediction

## Project Overview

This project converts transaction-level e-commerce data into a customer-level predictive analytics workflow. It uses historical customer behaviour, RFM features and Logistic Regression to estimate customer churn risk.

The project was prepared for the **IBM SkillsBuild Data Analytics with AI Academic Internship** project submission.

## Objective

The objective is to identify customers who may be at risk of churn and provide a practical risk level that can support customer-retention actions.

## Methodology

1. Load the cleaned transaction dataset.
2. Use **14-May-2026** as the historical cutoff date.
3. Use later transactions as the future observation period.
4. Create customer-level features:
   - Order Count
   - Total Revenue
   - Average Order Value
   - First Purchase
   - Last Purchase
   - Recency
   - Frequency
   - Monetary
5. Define churn as **no purchase during the future observation period**.
6. Train a Logistic Regression model using:
   - Recency
   - Frequency
   - Monetary
   - Avg_Order_Value
7. Evaluate the model using accuracy, precision, recall and a confusion matrix.
8. Generate churn probability and customer risk levels.

## Risk Levels

- **Low Risk:** churn probability < 40%
- **Medium Risk:** 40% to < 70%
- **High Risk:** >= 70%

## Results

The project report records:

- Accuracy: **67.24%**
- Precision: **68.75%**
- Recall: **70.97%**
- High Risk customers: **9**
- Medium Risk customers: **186**
- Low Risk customers: **37**

## Dataset

The repository includes:

`data/cleaned_customer_transactions.csv`

This is the cleaned **747-transaction** dataset used by the project. The project report states that the original dataset contained 2,000 rows and that data cleaning resulted in 747 usable transaction records and 304 unique customers.

The original 2,000-row source dataset is not included in this repository.

## Files

- `Customer_Churn_Prediction.ipynb` — complete Python/Jupyter Notebook
- `requirements.txt` — Python dependencies
- `README.md` — project documentation
- `data/cleaned_customer_transactions.csv` — cleaned transaction dataset
- `Masterclass_3_Final_Project_Report.docx` — project report
- `Masterclass_3_Final_Project_Output.xlsx` — project output

## How to Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Open the notebook

```bash
jupyter notebook Customer_Churn_Prediction.ipynb
```

### 3. Run all cells

The notebook creates:

`customer_churn_project_outputs.xlsx`

## Business Actions

The project identifies several possible retention actions, including:

- Prioritize high-risk customers for personalized retention campaigns.
- Send reminder or re-engagement messages to customers with long purchase gaps.
- Provide relevant product recommendations.
- Use loyalty incentives for low-frequency customers.
- Monitor high-value customers with elevated churn risk.

## Important Note

The predictions represent **risk estimates based on the available historical features**. They should be interpreted as associations and predicted risk rather than proof of the cause of churn.
