# saas-customer-retention-product-analytics
End-to-End SaaS Customer Retention &amp; Product Analytics Dashboard built using PostgreSQL, SQL, Power BI, and DAX.

# 🚀 SaaS Product Analytics & Customer Intelligence Platform

## 📌 Executive Summary

Customer retention is one of the most important growth drivers for SaaS businesses. While acquiring new customers is expensive, retaining existing customers directly increases Monthly Recurring Revenue (MRR), Customer Lifetime Value (CLV), and long-term business profitability. However, many SaaS organizations struggle to identify the underlying factors driving customer churn and the behaviors that predict long-term customer success.

This project presents an **end-to-end SaaS Product Analytics solution** that combines **PostgreSQL, SQL, Python, Statistical Hypothesis Testing, and Power BI** to analyze customer behavior, validate business hypotheses, and identify the key drivers of customer retention.

Instead of focusing only on dashboards, this project answers **10 critical business questions** related to customer churn, feature adoption, cohort performance, customer satisfaction, product engagement, and customer health. The project concludes by developing a **Customer Health Score**, enabling Customer Success teams to proactively identify high-risk customers before they churn.

The insights generated from this analysis provide actionable recommendations for **Product Managers, Customer Success Teams, Marketing Teams, and Executive Leadership**, enabling data-driven decisions that improve retention, customer engagement, and long-term revenue growth.

---

# 📌 Business Problem

The SaaS company is experiencing customer churn but lacks a clear understanding of the factors driving customer retention and customer loss. Although valuable customer data exists across subscriptions, product usage, customer support, and feedback systems, these datasets have not been integrated into a unified analytical framework capable of explaining customer behavior.

Without a data-driven understanding of churn drivers, Product and Customer Success teams risk making decisions based on assumptions rather than evidence. This can lead to ineffective retention strategies, poor resource allocation, and missed opportunities to retain high-value customers.

This project addresses that challenge by transforming raw operational data into actionable business intelligence using SQL-based analytics, statistical validation, customer behavior analysis, and predictive customer health scoring.

The objective is not only to understand **what happened**, but also explain **why it happened** and recommend **what the business should do next**.

---

# 📌 Project Objectives

This project was designed to answer the following business objectives:

- Assess the quality and reliability of customer data before performing analysis.
- Identify customer segments with the highest churn risk.
- Discover statistically significant drivers of customer retention.
- Evaluate customer engagement through product feature adoption.
- Measure customer retention trends using cohort analysis.
- Build a predictive Customer Health Score to identify at-risk customers.
- Identify an effective North Star Metric representing long-term product success.
- Deliver executive-ready dashboards to support strategic business decisions.

---

# 📊 Project Highlights

| Metric | Value |
|---------|-------|
| Industry | B2B SaaS |
| Customers Analyzed | **5,000** |
| Business Questions Answered | **10** |
| SQL Analysis Modules | **6+** |
| Statistical Tests Performed | **T-Test & Chi-Square Test** |
| Customer Health Score | ✅ Built |
| Executive Dashboard | ✅ Power BI |
| Database | PostgreSQL |
| Programming Language | Python |
| Visualization | Power BI |

---

# 🎯 Business Impact

This project enables business stakeholders to:

- Reduce customer churn through proactive intervention.
- Improve Customer Lifetime Value (CLV).
- Identify high-risk customers using predictive Customer Health Scores.
- Optimize customer onboarding and product adoption.
- Increase adoption of high-value product features.
- Validate business decisions using statistical hypothesis testing.
- Support Product, Customer Success, and Executive teams with actionable insights.

---

# 🛠 Tech Stack

| Category | Technologies |
|----------|--------------|
| Database | PostgreSQL |
| Query Language | SQL (CTEs, Joins, Window Functions, Aggregations, Views) |
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| Statistical Analysis | SciPy (T-Test, Chi-Square Test) |
| Machine Learning | Scikit-Learn (MinMaxScaler) |
| Data Visualization | Power BI |
| Development Environment | Jupyter Notebook |
| Database Connectivity | SQLAlchemy |

---

# 📂 Repository Structure

```text
📦 SaaS Product Analytics
│
├── 📂 SQL Scripts
│   ├── Churn_driver_analysis.sql
│   ├── Cohort_driver_analysis.sql
│   ├── Feature_Adoptation_driver_Analysis.sql
│   ├── Retention_Driver_Analysis.sql
│   ├── North_star_Metric.sql
│   └── View_summary.sql
│
├── 📂 Python Notebooks
│   ├── Data_Cleaning_and_Validation.ipynb
│   ├── Statistical_and_Hypothesis_Testing.ipynb
│   └── Health_Score.ipynb
│
├── 📂 Dashboard
│   └── SaaS Analytics Dashboard.pbix
│
└── README.md
```

---

# 📌 Business Questions & Answers

This project answers the following business questions using SQL, Python, Statistical Analysis, and Power BI:

1. Is the SaaS dataset reliable enough for business decision-making?
2. Which customer segments are most likely to churn?
3. Does account size (number of seats) significantly impact customer retention?
4. Are newer customer cohorts performing better?
5. Which product features drive the highest engagement and retention?
6. Does customer satisfaction prevent churn?
7. Does overall product usage dictate customer retention?
8. Do administrative features such as Auto-Renew reduce churn?
9. What is the most appropriate North Star Metric for long-term product success?
10. Can a Customer Health Score proactively identify customers at risk of churn?

We will look into it One by one.
# 📌 Business Questions & Answers

---

# 1. Is the SaaS dataset reliable enough for business decision-making?

## ✅ Business Answer

Yes. The dataset was successfully cleaned, validated, and transformed into a reliable analytical dataset before conducting business analysis. Data quality checks confirmed strong referential integrity, valid customer lifecycle timelines, and consistent relationships across customer, subscription, support, and feature usage data. Missing values were handled using appropriate imputation techniques to preserve statistical integrity without introducing analytical bias.

### 📊 Key Findings

- Analyzed **5,000 customer records** across multiple SaaS datasets.
- Missing values were identified primarily in **Customer Satisfaction** and **Support Ticket** attributes.
- Satisfaction scores were imputed using the **median** to preserve the original distribution.
- Missing support records represented customers with no support interactions rather than data quality issues.
- Revenue outliers were identified for further business review.
- Customer lifecycle validation confirmed no invalid signup or churn dates.
- Referential integrity checks verified consistency across all related datasets.

### 💡 Business Insights

- The dataset is sufficiently reliable for advanced analytics and statistical modeling.
- Missing support records reflect customer behavior rather than incomplete data.
- Strong data quality validation improves confidence in business decisions and predictive models.

### 🚀 Recommendations

- Implement automated data validation during data ingestion.
- Make customer satisfaction surveys mandatory after support interactions.
- Monitor revenue outliers regularly to identify pricing anomalies.
- Perform automated data quality checks before dashboard refreshes.

### 💰 Business Value

- Improves confidence in executive reporting.
- Prevents inaccurate business decisions caused by poor-quality data.
- Establishes a trusted foundation for churn prediction and customer analytics.

### 🛠 Technologies Used

- PostgreSQL
- SQL
- Python (Pandas)
- SQLAlchemy
- Jupyter Notebook

---

# 2. Which customer segments are most likely to churn?

## ✅ Business Answer

The analysis identified **Trial customers** and customers from the **DevTools industry** as the highest-risk segments for churn. Statistical testing further confirmed that **Subscription Plan Tier (Basic, Pro, Enterprise)** is **not a statistically significant predictor** of churn, indicating that customer engagement and onboarding play a much larger role than pricing plans.

### 📊 Key Findings

- Trial customers exhibited the highest churn rate.
- DevTools customers showed the highest churn among all industries.
- Subscription Plan Tier showed **no statistically significant relationship** with churn (**p = 0.059**).
- Customer lifecycle stage influenced churn more than subscription pricing.

### 💡 Business Insights

- Churn is primarily an onboarding and product adoption challenge rather than a pricing problem.
- Customers who fail to realize product value early are significantly more likely to leave.
- Industry-specific customer behavior should influence retention strategies.

### 🚀 Recommendations

- Redesign the trial onboarding experience.
- Build personalized onboarding flows for DevTools customers.
- Monitor customer engagement during the first 30 days.
- Trigger proactive Customer Success interventions for low-engagement trial users.

### 💰 Business Value

- Reduces early-stage customer churn.
- Improves customer activation and product adoption.
- Increases Customer Lifetime Value (CLV).
- Optimizes Customer Success resource allocation.

### 🛠 Technologies Used

- PostgreSQL
- SQL (Aggregations, CASE Statements)
- Python (SciPy Chi-Square Test)

---

# 3. Does account size (number of seats) significantly impact customer retention?

## ✅ Business Answer

No. Statistical analysis showed that account size, measured by the number of purchased seats, is **not a statistically significant predictor** of customer retention. Both retained and churned customers had similar average seat counts, suggesting that customer engagement and product value are stronger indicators of long-term retention.

### 📊 Key Findings

- Churned customers averaged **19.24 seats**.
- Retained customers averaged **20.93 seats**.
- Independent T-Test produced **p = 0.094**, indicating no statistically significant difference.
- Large enterprise customers are just as likely to churn if they fail to realize product value.

### 💡 Business Insights

- Customer size alone should not determine retention priority.
- Enterprise customers require continuous engagement despite larger contracts.
- Product adoption and customer satisfaction are more reliable indicators than seat count.

### 🚀 Recommendations

- Prioritize customer engagement over organization size.
- Monitor feature adoption regardless of account size.
- Develop Customer Success strategies using behavioral metrics instead of seat count.

### 💰 Business Value

- Prevents high-value enterprise accounts from being overlooked.
- Improves customer segmentation strategies.
- Enables more effective Customer Success prioritization.

### 🛠 Technologies Used

- PostgreSQL
- SQL (Aggregations, GROUP BY, Views)
- Python (SciPy Independent T-Test, Pandas, Numpy, SQLAlchemy, matplotlib, searborn)
- # 4. Are newer customer cohorts performing better?

## ✅ Business Answer

Yes. Cohort Analysis revealed that customer retention has improved significantly across newer acquisition cohorts. Customers acquired in late 2024 demonstrated higher retention rates, stronger product engagement, and higher Monthly Recurring Revenue (MRR), indicating that recent product enhancements and onboarding improvements have positively influenced long-term customer success.

### 📊 Key Findings

- Customer retention improved from approximately **76% in 2023** to **81%+ in 2024**.
- **December 2024** recorded the highest retention rate at **94.12%**.
- Recent cohorts generated higher average MRR.
- Newer customers adopted more product features compared to earlier cohorts.

### 💡 Business Insights

- Improvements introduced during 2024 positively impacted customer retention.
- Enhanced onboarding and product adoption strategies are attracting higher-quality customers.
- Continuous cohort monitoring helps evaluate the long-term effectiveness of business initiatives.

### 🚀 Recommendations

- Standardize onboarding practices introduced during high-performing cohorts.
- Analyze successful acquisition channels responsible for improved retention.
- Continuously monitor cohort performance to identify declining trends early.

### 💰 Business Value

- Improves long-term customer retention.
- Increases Customer Lifetime Value (CLV).
- Maximizes return on customer acquisition investments.

### 🛠 Technologies Used

- PostgreSQL
- SQL (Cohort Analysis, DATE_TRUNC, Window Functions)
- Power BI

---

# 5. Which product features drive the highest engagement and retention?

## ✅ Business Answer

Feature Adoption Analysis showed that high feature usage does not necessarily translate into higher customer retention. While **Feature 32** recorded the highest overall usage, **Feature 23** demonstrated the strongest association with retained customers despite its relatively low adoption rate. This suggests that feature value is more important than feature popularity.

### 📊 Key Findings

- Feature 32 recorded the highest overall usage.
- Feature 23 had the lowest adoption but the strongest association with retained customers.
- Beta features showed minimal influence on customer retention.
- Product engagement varied significantly across customer segments.

### 💡 Business Insights

- Highly valuable features may remain undiscovered by many customers.
- Feature popularity should not be used as the sole measure of product success.
- Increasing adoption of high-value features can improve long-term customer retention.

### 🚀 Recommendations

- Improve discovery of Feature 23 through onboarding and in-app guidance.
- Launch feature education campaigns targeting existing customers.
- Track feature adoption as a leading indicator of customer engagement.

### 💰 Business Value

- Improves product engagement.
- Increases customer retention without requiring new feature development.
- Supports product-led growth initiatives.

### 🛠 Technologies Used

- PostgreSQL
- SQL (JOINs, Aggregations)
- Power BI

---

# 6. Does customer satisfaction prevent churn?

## ✅ Business Answer

Yes. Statistical analysis confirmed that customer satisfaction is a significant predictor of customer retention. Customers with higher satisfaction scores were significantly more likely to remain active. In contrast, reducing support resolution time alone did not have a meaningful impact on customer churn.

### 📊 Key Findings

- Customer Satisfaction demonstrated statistical significance (**p = 0.0033**).
- Higher satisfaction scores were associated with retained customers.
- Average Resolution Time showed only a weak relationship with retention.
- Customer experience had a greater impact than operational efficiency alone.

### 💡 Business Insights

- Customer satisfaction is a stronger retention driver than ticket resolution speed.
- Delivering high-quality support experiences improves long-term customer loyalty.
- Measuring only operational KPIs may overlook critical customer experience issues.

### 🚀 Recommendations

- Prioritize Customer Satisfaction (CSAT) as a primary Customer Success KPI.
- Collect customer feedback after every support interaction.
- Monitor satisfaction trends alongside churn metrics.

### 💰 Business Value

- Improves customer loyalty.
- Reduces churn.
- Supports customer-centric decision making.

### 🛠 Technologies Used

- PostgreSQL
- SQL
- Python (SciPy T-Test)

  # 7. Does overall product usage dictate customer retention?

## ✅ Business Answer

Yes. Overall product usage emerged as one of the strongest indicators of customer retention. Statistical testing confirmed that customers who actively engaged with product features were significantly more likely to remain subscribed.

### 📊 Key Findings

- Feature Usage demonstrated the strongest statistical relationship with retention (**p = 2.42 × 10⁻⁵**).
- Customers with higher product engagement exhibited lower churn rates.
- Product usage consistently outperformed administrative metrics as a predictor of retention.

### 💡 Business Insights

- Product adoption directly influences customer retention.
- Customers who integrate the product into daily workflows are less likely to churn.
- Behavioral metrics are more valuable than subscription attributes.

### 🚀 Recommendations

- Monitor Daily Active Users (DAU) and Weekly Active Users (WAU).
- Trigger proactive engagement campaigns when product usage declines.
- Encourage adoption of core product features.

### 💰 Business Value

- Enables proactive churn prevention.
- Improves customer engagement.
- Increases long-term recurring revenue.

### 🛠 Technologies Used

- Python (SciPy T-Test)
- Pandas
- SQL

---

# 8. Do administrative features such as Auto-Renew reduce churn?

## ✅ Business Answer

No. Statistical testing demonstrated that Auto-Renew status has little influence on customer retention. Customers continue to churn when they fail to realize sufficient product value, regardless of billing preferences.

### 📊 Key Findings

- Auto-Renew showed **no statistically significant relationship** with churn (**p = 0.85**).
- Customers actively managed their subscriptions regardless of renewal settings.
- Product value remained the primary driver of retention.

### 💡 Business Insights

- Billing configuration alone cannot retain dissatisfied customers.
- Sustainable retention depends on product value rather than contractual friction.

### 🚀 Recommendations

- Focus Customer Success initiatives on product adoption.
- Increase customer engagement instead of relying on billing mechanisms.
- Measure customer value using behavioral analytics.

### 💰 Business Value

- Supports product-led growth.
- Improves customer experience.
- Prevents investment in ineffective retention tactics.

### 🛠 Technologies Used

- Python (SciPy Chi-Square Test)
- Pandas
- SQL

---

# 9. What is the most appropriate North Star Metric for measuring long-term product success?

## ✅ Business Answer

No single engagement metric consistently explained long-term customer retention. Product activity alone is insufficient for measuring customer success. A composite metric combining Customer Health Score, Feature Adoption, and Customer Satisfaction provides a more meaningful representation of long-term business value.

### 📊 Key Findings

- Total Feature Usage alone was insufficient.
- Usage Duration alone was insufficient.
- Feature Diversity alone was insufficient.
- Seat Count alone was insufficient.
- Customer Health Score provides a more comprehensive indicator.

### 💡 Business Insights

- Single engagement metrics can be misleading.
- Customer value should be measured across multiple behavioral dimensions.
- Composite metrics provide better executive visibility.

### 🚀 Recommendations

- Develop a composite North Star Metric.
- Combine Health Score, Customer Satisfaction, and Feature Adoption.
- Review North Star Metric performance periodically.

### 💰 Business Value

- Supports strategic product decisions.
- Improves executive reporting.
- Aligns product success with customer value.

### 🛠 Technologies Used

- SQL
- Python
- Power BI
- # 10. Can a Customer Health Score proactively identify customers at risk of churn?

## ✅ Business Answer

Yes. A Customer Health Score was developed by combining Customer Satisfaction, Feature Usage, Monthly Recurring Revenue (MRR), Product Errors, and Support Tickets into a weighted scoring model. The model successfully identified customers at higher churn risk, although score thresholds require recalibration for improved segmentation.

### 📊 Key Findings

- Health Score Components:
  - Customer Satisfaction (30%)
  - Feature Usage (25%)
  - MRR (20%)
  - Product Errors (15%)
  - Support Tickets (10%)
- Initial scoring classified most customers as High Risk.
- Score distribution indicated threshold recalibration is required.

### 💡 Business Insights

- Customer Health Scores enable proactive customer management.
- Multiple customer behaviors provide stronger predictive power than individual metrics.
- Threshold optimization will improve model accuracy.

### 🚀 Recommendations

- Recalibrate Health Score thresholds using historical retention data.
- Integrate Health Scores into Customer Success workflows.
- Monitor Health Scores continuously through executive dashboards.

### 💰 Business Value

- Enables early identification of at-risk customers.
- Supports proactive retention strategies.
- Improves Customer Success efficiency.

### 🛠 Technologies Used

- Python
- Pandas
- Scikit-Learn (MinMaxScaler)
- SQL
- Power BI

---

# 📈 Overall Business Outcomes

This project successfully transformed raw SaaS operational data into actionable business intelligence by integrating SQL analytics, statistical hypothesis testing, customer behavior analysis, and executive dashboarding.

### Key Business Outcomes

- Built a unified Customer 360 analytical framework.
- Identified key drivers of customer churn and retention.
- Validated business assumptions using statistical hypothesis testing.
- Measured customer retention trends through cohort analysis.
- Evaluated feature adoption to identify high-value product capabilities.
- Developed a predictive Customer Health Score for proactive risk identification.
- Designed an interactive Power BI dashboard for executive decision-making.

---

# 📊 Dashboard Overview

The Power BI dashboard enables business stakeholders to monitor:

- Executive KPIs
- Customer Health Score Distribution
- Customer Churn Analysis
- Retention Trends
- Cohort Performance
- Feature Adoption
- Revenue Performance
- Customer Segmentation

---

# 🏗 Project Architecture

```text
Raw SaaS Data
        │
        ▼
 PostgreSQL Database
        │
        ▼
 SQL Data Extraction & Transformation
        │
        ▼
 Python Data Analysis & Statistical Testing
        │
        ▼
 Customer Health Score Development
        │
        ▼
 Interactive Power BI Dashboard
        │
        ▼
 Business Insights & Strategic Recommendations
```

---

# 🚀 Future Enhancements

- Develop a Machine Learning churn prediction model.
- Automate Customer Health Score updates using scheduled pipelines.
- Integrate real-time product usage events.
- Deploy automated retention alerts for Customer Success teams.
- Expand dashboard with executive forecasting and anomaly detection.
