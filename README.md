I am working on a customer churn prediction project from the BCG Data Science Job Simulation and need guidance on building a robust machine learning model.

Project Context:
The goal is to understand whether changes in electricity pricing influence customer churn and to build a predictive model that identifies customers likely to leave.

Data Overview:
The dataset contains approximately 14,600 customers. Each row represents a single customer after merging two datasets:

1. client_data – customer characteristics, consumption, contract information
2. price_data – historical electricity price records aggregated into customer-level features

Target Variable:

* churn (binary)

  * 0 = customer stayed
  * 1 = customer churned

Data Preparation Completed:
I have already performed EDA and feature engineering.

Steps completed:

* handled missing values
* converted date columns to datetime
* engineered contract-related features
* aggregated price data by customer id
* merged price features with client data
* encoded categorical variables (channel_sales and origin_up)
* converted boolean variables to numeric
* removed the id column after merging

Engineered Features Include:
Customer behavior features

* cons_12m
* cons_last_month
* avg_monthly_consumption
* consumption_trend

Contract features

* tenure_days
* tenure_years
* days_since_mod
* days_to_renewal
* num_years_antig

Product features

* nb_prod_act
* has_gas

Financial features

* net_margin
* margin_net_pow_ele
* margin_gross_pow_ele

Price sensitivity features (aggregated from price_data)

* mean price
* max price
* min price
* price change
* price volatility

Categorical encodings

* channel_sales_*
* origin_up_*

Dataset Characteristics:

* ~14,600 rows
* ~35–45 features
* class imbalance (about 10% churn)

Modeling Goals:

1. Build a predictive model to estimate churn probability
2. Identify the most important drivers of churn
3. Evaluate model performance using appropriate metrics
4. Apply the model to generate predictions for a separate dataset called data_for_predictions.csv

What I need help with:

1. Designing a proper ML pipeline for churn prediction
2. Recommended models for this dataset (Logistic Regression, Random Forest, Gradient Boosting, etc.)
3. Handling class imbalance
4. Selecting the most important features
5. Evaluating model performance using metrics such as:

   * ROC-AUC
   * precision
   * recall
   * F1 score
6. Interpreting feature importance for business insights
7. Generating predictions for new customers

Please explain each step in a clear modeling workflow and provide reasoning for the model choices.
