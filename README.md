# Predictive Analytics for High-Value Customer Churn in the Telecom Sector Using Machine Learning

## Project Objective:
The primary goal of this project is to develop predictive models to identify high-value prepaid customers at risk of churn for a leading telecom operator in the Indian and Southeast Asian markets. This is crucial in reducing customer attrition, as retaining existing customers is significantly more cost-effective than acquiring new ones. Additionally, the project aims to identify key indicators of churn to inform targeted customer retention strategies.

## Business Context:
**Industry Dynamics:**
- The telecom industry experiences an annual churn rate of 15–25%.
- Customer retention is prioritized over acquisition due to its cost-effectiveness (5–10 times cheaper).
  
**Churn Definition:**
- In the prepaid model, churn is defined as zero outgoing/incoming calls and zero data usage over a defined period, differentiating temporary inactivity from actual churn.
  
**Focus on High-Value Customers:**
- Approximately 80% of revenue is derived from the top 20% of customers, making the retention of high-value customers critical.
  
**Customer Behavior:**
The customer lifecycle includes three phases:
- **Good Phase:** Regular usage without service issues.
- **Action Phase:** Decline in usage due to dissatisfaction or external offers.
- **Churn Phase:** Complete cessation of services.
  
## Dataset Overview:
- Data spans four months (June to September), encoded as months 6, 7, 8, and 9.
- Attributes include recharge amounts, call usage (incoming and outgoing), and mobile internet data usage (2G/3G).
- The business task is to predict churn in the fourth month using data from the first three months.

## Methodology:
**1. Data Preparation:**

- **Derived New Features:** Created features based on recharge frequency, drop in usage metrics, and average monthly usage - patterns to enhance model accuracy.
- **High-Value Customer Segmentation:** Identified high-value customers as those with recharge amounts above the 70th percentile in the first two months.
- **Churn Tagging:** Defined churn based on zero usage metrics for calls and data in the fourth month.
- **Data Cleaning:** Removed attributes corresponding to the churn phase (month 9) to prevent data leakage.
  
**2. Exploratory Data Analysis (EDA):**
- Analyzed customer behavior across the three phases of the lifecycle.
- Identified trends in call and data usage, highlighting sharp declines in the action phase as a precursor to churn.
- Visualized recharge patterns and frequency for high-value customers.

**3. Feature Engineering and Dimensionality Reduction:**
- Engineered features such as average usage trends, variance in usage, and monthly growth/decline in recharges.
- Reduced dimensionality using Principal Component Analysis (PCA) to retain significant information while simplifying the feature space.

**4. Model Building:**
Trained several classification models, including:
- Logistic Regression
- Random Forest
- Gradient Boosting (e.g., XGBoost)
 **Addressed class imbalance using:**
- SMOTE (Synthetic Minority Oversampling Technique)
- Class-weighted algorithms
- Prioritized recall over precision to maximize identification of churners.

**5. Feature Importance Analysis:**
- Used Logistic Regression coefficients and Decision Tree feature importance metrics to identify top predictors.
- Highlighted factors like a decline in data usage, recharge frequency, and call volume as critical churn indicators.

## Evaluation Metrics:
**Model Metrics:**
- Precision, Recall, F1-Score
- ROC-AUC Curve
  
**Business Focus:**
- Higher recall ensures a greater proportion of at-risk customers are correctly identified.

## Results and Insights:
**Model Performance:**
- Achieved a recall of 85% on high-value customer churn prediction, with an overall ROC-AUC score of 90%.
  
**Key Predictors of Churn:**
- Significant drop in mobile data usage.
- Decrease in outgoing call volumes over time.
- Reduced recharge amounts and frequency.
  
**Business Insights:**
- High-value customers show a noticeable decline in usage during the action phase, providing an opportunity for intervention.
- Proactive engagement strategies and personalized offers can effectively address churn risks.

## Recommendations:
**Retention Strategies:**
- Offer exclusive plans, loyalty rewards, and discounts to customers exhibiting signs of churn during the action phase.
- Improve customer service touchpoints to address dissatisfaction promptly.
  
**Proactive Engagement:**
- Monitor high-value customer activity to detect early signs of churn.
- Launch targeted campaigns based on usage trends and customer segmentation.
  
**Service Improvements:**
- Enhance service quality in regions with high churn rates.
- Address common customer pain points identified through the analysis.

## Tools and Techniques:
- **Data Processing:** Python (Pandas, NumPy), SQL.
- **Visualization:** Matplotlib, Seaborn, Plotly.
- **Modeling:** Scikit-learn, XGBoost, Random Forest.
- **Dimensionality Reduction:** PCA.
- **Class Imbalance Handling:** SMOTE, Class-weighted algorithms.

## Outcome:
The project successfully developed a robust churn prediction system that enables the telecom operator to:
- Anticipate churn among high-value customers with high accuracy.
- Implement targeted retention strategies to reduce revenue leakage.
- Understand the primary factors influencing churn for better decision-making.

## Dataset:
https://drive.google.com/file/d/1SWnADIda31mVFevFcfkGtcgBHTKKI94J/view
