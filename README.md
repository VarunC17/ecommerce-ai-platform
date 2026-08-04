# ECOMMERCE-AI-PLATFORM

## Overview

ECOMMERCE-AI-PLATFORM is an end-to-end data analytics, machine learning, and business intelligence project built using the Brazilian Olist E-commerce dataset. The project demonstrates the complete analytics lifecycle, including data ingestion, cleaning, feature engineering, SQL analytics, predictive modeling, recommendation systems, forecasting, AI-generated business insights, and interactive reporting using Power BI.

The project was developed as a portfolio project to demonstrate practical skills in data engineering, machine learning, data visualization, and business intelligence.

---

## Project Objectives

The primary objectives of this project are to:

- Build a complete data analytics pipeline from raw data to dashboard.
- Perform exploratory data analysis on e-commerce transactions.
- Engineer meaningful customer, product, and seller features.
- Develop customer segmentation using machine learning.
- Predict customer churn.
- Estimate customer lifetime value.
- Build a product recommendation system.
- Generate sales forecasts.
- Produce AI-generated business insights.
- Design an interactive Power BI dashboard for executive reporting.

---

## Dataset

**Dataset:** Brazilian Olist E-commerce Dataset

The dataset contains information about:

- Customers
- Orders
- Order Items
- Payments
- Reviews
- Products
- Sellers
- Geolocation

The dataset was cleaned, transformed, and loaded into PostgreSQL before being used for analytics and machine learning.

---

## Project Architecture

```
Raw CSV Files
      │
      ▼
Data Loading
      │
      ▼
Data Cleaning
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Feature Engineering
      │
      ▼
PostgreSQL Data Warehouse
      │
      ▼
SQL Business Analytics
      │
      ▼
Machine Learning Models
      │
      ├── Customer Segmentation
      ├── Customer Lifetime Value
      ├── Customer Churn Prediction
      ├── Recommendation System
      └── Sales Forecasting
      │
      ▼
AI Insight Generation
      │
      ▼
Dashboard Data Preparation
      │
      ▼
Power BI Dashboard
```

---

## Technologies Used

### Programming

- Python 3.12

### Data Processing

- Pandas
- NumPy

### Machine Learning

- Scikit-learn

### Data Visualization

- Matplotlib
- Plotly
- Power BI Desktop

### Database

- PostgreSQL
- SQLAlchemy
- psycopg2
- pgAdmin

### Development Tools

- Jupyter Notebook
- Git
- GitHub

---

## Project Structure

```
ECOMMERCE-AI-PLATFORM
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── predictions/
│
├── models/
│
├── notebooks/
│   ├── 01_project_setup.ipynb
│   ├── 02_data_loading.ipynb
│   ├── 03_data_cleaning.ipynb
│   ├── 04_exploratory_data_analysis.ipynb
│   ├── 05_load_cleaned_data_to_postgresql.ipynb
│   ├── 06_sql_business_analysis.ipynb
│   ├── 07_feature_engineering.ipynb
│   ├── 08_sales_analytics.ipynb
│   ├── 09_customer_segmentation.ipynb
│   ├── 10_customer_lifetime_value.ipynb
│   ├── 11_customer_churn_prediction.ipynb
│   ├── 12_product_recommendation_system.ipynb
│   ├── 13_sales_forecasting.ipynb
│   ├── 14_ai_insights.ipynb
│   └── 15_dashboard_data_preparation.ipynb
│
├── reports/
│   ├── powerbi/
│   ├── dashboard_documentation/
│   └── screenshots/
│
├── requirements.txt
├── README.md
├── LICENSE
└── .gitignore
```

---

## Machine Learning Components

### Customer Segmentation

Customer segmentation was performed using clustering techniques to group customers based on purchasing behavior.

Outputs include:

- Customer clusters
- Segment names
- Cluster statistics

---

### Customer Lifetime Value

Estimated customer value using historical purchasing behavior.

Outputs include:

- Historical CLV
- Estimated Future CLV
- Customer value segments

---

### Customer Churn Prediction

Machine learning models were used to identify customers likely to stop purchasing.

Outputs include:

- Churn probability
- Risk level
- Churn prediction

---

### Product Recommendation System

Generated personalized product recommendations based on customer purchase history.

Outputs include:

- Recommended products
- Recommendation score
- Recommendation ranking

---

### Sales Forecasting

Historical sales were analyzed to support future business planning.

Outputs include:

- Historical sales trends
- Forecast periods
- Forecast models
- Transaction summaries

---

### AI Business Insights

Automatically generated business insights summarize important analytical findings and identify strategic business opportunities.

Outputs include:

- Business insights
- KPI summaries
- Strategic opportunities

---

## Power BI Dashboard

The project includes a seven-page interactive Power BI dashboard.

### Dashboard Pages

1. Executive Overview
2. Sales Analytics
3. Customer Analytics
4. Customer Churn
5. Recommendation System
6. Sales Forecasting
7. AI Insights

The dashboard integrates business intelligence, machine learning outputs, forecasting, and AI-generated insights into a single reporting solution.

---

## Dashboard Features

- Interactive KPI cards
- Cross-filtering
- Dynamic slicers
- Geographic analysis
- Customer analytics
- Product analytics
- Forecast visualizations
- Recommendation analytics
- AI-generated insights
- Executive reporting

---

## Database

Database Management System:

PostgreSQL

Database Name:

```
ecommerce_ai_db
```

Primary reporting schema:

```
dashboard
```

The PostgreSQL database stores cleaned data, engineered features, machine learning outputs, recommendation results, forecasting data, AI insights, and dashboard-ready tables.

---

## Business Value

The project demonstrates how analytics and machine learning can be applied to solve common business problems, including:

- Revenue monitoring
- Customer segmentation
- Customer retention
- Customer lifetime value estimation
- Product recommendations
- Sales forecasting
- Executive reporting
- Business opportunity identification

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Data Cleaning
- Feature Engineering
- SQL
- PostgreSQL
- Data Warehousing
- Exploratory Data Analysis
- Machine Learning
- Customer Analytics
- Recommendation Systems
- Predictive Analytics
- Business Intelligence
- Power BI
- DAX
- Git
- GitHub

---

## Installation

### Clone the repository

```bash
git clone https://github.com/<your-username>/ECOMMERCE-AI-PLATFORM.git
```

---

### Create a virtual environment

```bash
python -m venv venv
```

Windows

```bash
venv\Scripts\activate
```

Linux / macOS

```bash
source venv/bin/activate
```

---

### Install dependencies

```bash
pip install -r requirements.txt
```

---

### Configure PostgreSQL

Create a PostgreSQL database named:

```
ecommerce_ai_db
```

Update the database connection settings in the notebooks as required.

---

### Run the notebooks

Execute the notebooks sequentially:

```
01_project_setup.ipynb

02_data_loading.ipynb

03_data_cleaning.ipynb

04_exploratory_data_analysis.ipynb

05_load_cleaned_data_to_postgresql.ipynb

06_sql_business_analysis.ipynb

07_feature_engineering.ipynb

08_sales_analytics.ipynb

09_customer_segmentation.ipynb

10_customer_lifetime_value.ipynb

11_customer_churn_prediction.ipynb

12_product_recommendation_system.ipynb

13_sales_forecasting.ipynb

14_ai_insights.ipynb

15_dashboard_data_preparation.ipynb
```

Finally, open the Power BI dashboard located in:

```
reports/powerbi/
```

---

## Future Improvements

Possible future enhancements include:

- Real-time data ingestion
- Power BI Service deployment
- Scheduled data refresh
- Cloud-based PostgreSQL deployment
- Advanced recommendation algorithms
- Deep learning forecasting models
- Automated anomaly detection
- Natural language query support
  
---

## Author

Developed by **Varun Contractor** as an end-to-end data analytics, machine learning, and business intelligence portfolio project demonstrating practical applications of data engineering, predictive analytics, and interactive reporting.
