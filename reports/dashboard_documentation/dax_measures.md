# Revenue Measures

```DAX
Total Revenue =
SUM('Fact Sales'[total_order_value])
```

```DAX
Monthly Revenue =
CALCULATE(
    [Total Revenue],
    DATESMTD('Dim Calendar'[date])
)
```

```DAX
Yearly Revenue =
CALCULATE(
    [Total Revenue],
    DATESYTD('Dim Calendar'[date])
)
```

```DAX
Revenue Growth % =
VAR CurrentRevenue = [Total Revenue]
VAR PreviousRevenue =
    CALCULATE(
        [Total Revenue],
        DATEADD('Dim Calendar'[date], -1, YEAR)
    )
RETURN
DIVIDE(CurrentRevenue - PreviousRevenue, PreviousRevenue)
```

```DAX
Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders]
)
```

---

# Order Measures

```DAX
Total Orders =
DISTINCTCOUNT('Fact Sales'[order_id])
```

---

# Customer Measures

```DAX
Total Customers =
DISTINCTCOUNT('Dim Customer'[customer_id])
```

```DAX
Active Customers =
CALCULATE(
    DISTINCTCOUNT('Dim Customer'[customer_id]),
    'Fact Customer Features'[total_orders] > 0
)
```

```DAX
Average Customer Spend =
AVERAGE('Fact Customer Features'[total_spend])
```

```DAX
Average Orders =
AVERAGE('Fact Customer Features'[total_orders])
```

```DAX
Average Customer Lifetime =
AVERAGE('Fact Customer Features'[customer_lifetime_days])
```

---

# CLV Measures

```DAX
Average CLV =
AVERAGE('Fact Customer CLV'[historical_clv])
```

```DAX
Total Historical CLV =
SUM('Fact Customer CLV'[historical_clv])
```

```DAX
Estimated Future CLV =
SUM('Fact Customer CLV'[estimated_future_clv])
```

---

# Churn Measures

```DAX
Churn Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS('Fact Customer Churn'),
        'Fact Customer Churn'[churn_prediction] = 1
    ),
    COUNTROWS('Fact Customer Churn')
)
```

```DAX
Retention Rate =
1 - [Churn Rate]
```

```DAX
High Risk Customers =
CALCULATE(
    COUNTROWS('Fact Customer Churn'),
    'Fact Customer Churn'[risk_level] = "High"
)
```

```DAX
Average Churn Probability =
AVERAGE('Fact Customer Churn'[churn_probability])
```

---

# Customer Segmentation

```DAX
Segment Revenue =
SUM('Fact Customer Segmentation'[total_spend])
```

---

# Recommendation Measures

```DAX
Total Recommendations =
COUNTROWS('Fact Recommendations')
```

```DAX
Average Recommendation Score =
AVERAGE('Fact Recommendations'[recommendation_score])
```

```DAX
Recommendation Methods =
DISTINCTCOUNT(
    'Fact Recommendations'[recommendation_method]
)
```

```DAX
Customers Receiving Recommendations =
DISTINCTCOUNT(
    'Fact Recommendations'[customer_id]
)
```

```DAX
Recommendation Count =
COUNT('Fact Recommendations'[recommended_product_id])
```

---

# Forecast Measures

```DAX
Forecast Records =
COUNTROWS('Fact Sales Forecast')
```

```DAX
Forecast Models =
DISTINCTCOUNT(
    'Fact Sales Forecast'[model_name]
)
```

```DAX
Forecast Frequencies =
DISTINCTCOUNT(
    'Fact Sales Forecast'[forecast_frequency]
)
```

```DAX
Total Forecast Transactions =
SUM(
    'Fact Sales Forecast'[transactions]
)
```

---

# AI Measures

```DAX
Total AI Insights =
COUNTROWS('AI Insights')
```

```DAX
High Priority Insights =
CALCULATE(
    COUNTROWS('AI Insights'),
    'AI Insights'[priority] = "High"
)
```

```DAX
Total Opportunities =
COUNTROWS('AI Opportunities')
```

```DAX
Total KPI Metrics =
COUNTROWS('dashboard_kpi_metrics')
```

---

# Product Measures (Recommended)

These weren't all created during the dashboard build, but I recommend adding them because they make the model more complete.

```DAX
Total Products =
DISTINCTCOUNT('Dim Product'[product_id])
```

```DAX
Product Revenue =
SUM('Fact Product Analytics'[total_revenue])
```

```DAX
Average Product Revenue =
AVERAGE('Fact Product Analytics'[total_revenue])
```

---

# Seller Measures

```DAX
Total Sellers =
DISTINCTCOUNT('Dim Seller'[seller_id])
```

```DAX
Seller Revenue =
SUM('Fact Seller Analytics'[total_revenue])
```
