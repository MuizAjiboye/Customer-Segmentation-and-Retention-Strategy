# Customer Segmentation & Retention Strategy Analysis
## Executive Summary
An online retailer wanted to better understand customer purchasing behaviour, identify customers at risk of churn, and develop targeted retention and loyalty strategies.
Using over **525,000 retail transactions**, customers were segmented based on purchasing behaviour using the **RFM Framework (Recency, Frequency, and Monetary Value)**. The analysis identified seven distinct customer groups ranging from inactive customers requiring re-engagement to highly valuable customers responsible for a disproportionate share of revenue.
The results provide a framework for improving customer retention, increasing customer lifetime value, and optimizing marketing spend through personalized engagement strategies.

---
## Business Problem
Not all customers contribute equally to business growth.
Applying the same marketing strategy to every customer often results in inefficient spending and missed opportunities. Leadership wanted answers to several key questions:
- Which customers generate the most value?
- Which customers are at risk of churn?
- Which customers should receive loyalty rewards?
- Where should retention efforts be prioritized?
- How can marketing campaigns be personalized for different customer groups?
To answer these questions, customer purchasing behaviour was analyzed using the RFM framework.
---
## Dataset Overview
### Source
**Online Retail II Dataset**
### Time Period
December 2009 – December 2010
### Original Dataset
| Metric | Value |
|---|---:|
| Transaction Records | 525,461 |
| Invoices | 28,816 |
| Stock Codes | 4,632 |
| Countries | 40 |
### Key Variables
- Invoice Number
- Product Code
- Product Description
- Quantity Purchased
- Purchase Date
- Unit Price
- Customer ID
- Country
---
## Data Quality Challenges
Initial exploration identified several issues that could distort customer segmentation results.
### 1. Invalid Transactions
The dataset contained records representing:
- Product returns and cancellations
- Shipping charges
- Discounts
- Bank charges
- Administrative adjustments
- Manual transactions
- Testing records
Because these records do not represent genuine customer purchasing behaviour, they were excluded from the analysis.
### 2. Missing Customer IDs
More than 100,000 transactions contained missing customer identifiers.
Since customer-level analysis requires unique customer identification, these records were removed.
### 3. Invalid Pricing Records
Transactions with zero or invalid pricing values were excluded to prevent distortion of customer value calculations.
### Data Preparation Outcome
Approximately **23% of records were removed during cleaning** to ensure reliable customer segmentation.
---
## Analytical Approach
### Customer Behaviour Framework
Customers were evaluated using three metrics commonly used in retail and customer analytics.
| Metric | Definition |
|---|---|
| **Recency** | How recently a customer made a purchase |
| **Frequency** | How often a customer purchases |
| **Monetary Value** | How much revenue a customer generates |
These metrics were aggregated to create a customer-level behavioural profile.
### Outlier Analysis
Customer spending behaviour was heavily skewed.
A relatively small group of customers generated substantially higher revenue and purchased significantly more frequently than the broader customer base.
To improve segmentation quality, outliers were identified using the **Interquartile Range (IQR) method**.
Outliers were removed from the clustering process and analyzed separately as strategic customer groups.
This ensured that high-value customers did not distort cluster formation for the majority of customers.
### Customer Segmentation
Customer profiles were standardized and segmented using **K-Means clustering**.
The optimal number of clusters was determined using:
- Elbow Method
- Silhouette Score
The analysis identified four behavioural customer segments among the standard customer population and three additional high-value customer groups.
---
## Key Findings
### 1. REWARD — Loyal, High-Value Customers
**Characteristics**
- Highest customer value
- Highest purchase frequency
- Consistently active
**Why This Matters**
These customers represent the retailer's most loyal and profitable customer segment.
**Recommendations**
- Loyalty rewards
- Exclusive promotions
- Early access to products
- VIP experiences
### 2. RETAIN — Valuable Customers to Protect
**Characteristics**
- Strong purchasing behaviour
- Consistent spending
- Recently active
**Why This Matters**
These customers already provide substantial revenue and should be protected from churn.
**Recommendations**
- Personalized recommendations
- Retention campaigns
- Cross-selling initiatives
- Loyalty incentives
### 3. NURTURE — Customers with Growth Potential
**Characteristics**
- Lower spending
- Lower purchase frequency
- Recent purchasing activity
**Why This Matters**
These customers demonstrate growth potential and may become more valuable over time.
**Recommendations**
- Product education
- Welcome journeys
- Relationship-building campaigns
- Repeat-purchase incentives
### 4. RE-ENGAGE — Customers at Risk of Churn
**Characteristics**
- Low spending
- Low purchase frequency
- Long period since last purchase
**Why This Matters**
These customers appear to be at risk of churn.
**Recommendations**
- Win-back campaigns
- Reactivation emails
- Promotional offers
- Customer outreach initiatives
---
## High-Value Customer Analysis
Several customers behaved significantly differently from the wider customer base and were analyzed separately.
### 5. DELIGHT — Exceptional Customer Value
**Characteristics**
- Extremely high spending
- Extremely high purchase frequency
**Why This Matters**
These customers represent the retailer's most valuable customer relationships.
**Recommendations**
- VIP treatment
- Dedicated customer support
- Exclusive offers
- Priority service
### 6. PAMPER — High-Spending Customers
**Characteristics**
- Very high spending
- Lower purchase frequency
**Why This Matters**
These customers make large purchases and contribute significant revenue despite purchasing less frequently.
**Recommendations**
- Premium customer experiences
- Personalized engagement
- High-value product recommendations
### 7. UPSELL — Opportunities to Increase Basket Value
**Characteristics**
- High purchase frequency
- Lower average spend
**Why This Matters**
These customers are highly engaged and provide opportunities to increase average order value.
**Recommendations**
- Product bundles
- Cross-selling strategies
- Basket value optimization
---
## Strategic Insights
### 1. Customer Value Is Highly Concentrated
A relatively small proportion of customers generate a disproportionately large share of revenue.
**Business Implication:** Protecting high-value customer relationships can have a significant impact on revenue performance.
### 2. Different Customers Require Different Strategies
Customer behaviour varies significantly across segments.
**Business Implication:** Applying the same marketing strategy to every customer reduces effectiveness and wastes resources.
### 3. Retention Represents a Significant Growth Opportunity
Several existing customer groups already demonstrate strong purchasing behaviour.
**Business Implication:** Improving retention can often generate greater returns than acquiring additional customers, depending on acquisition costs, retention costs, and customer lifetime value.

---
## Business Recommendations
| Business Function | Recommendation |
|---|---|
| **Marketing Team** | Develop customer segment-specific campaigns rather than broad, one-size-fits-all promotions. |
| **CRM Team** | Implement automated engagement journeys tailored to the behaviour of each segment. |
| **Customer Success Team** | Prioritize retention efforts for high-value customer groups. |
| **Leadership Team** | Allocate resources toward segments with the largest revenue impact and greatest retention opportunities. |
---
## Business Impact
This analysis enables the business to:
- Identify high-value customers
- Detect customers at risk of churn
- Improve customer retention
- Increase customer lifetime value
- Optimize marketing spend
- Personalize customer engagement
- Create a scalable customer intelligence framework
---
## Skills Demonstrated
### Business & Analytical Skills
- Customer Segmentation
- RFM Analysis
- Customer Retention Analytics
- Customer Lifetime Value Analysis
- Customer Behaviour Analysis
- Retail Analytics
- Business Intelligence
- Marketing Analytics
- Data Storytelling
### Technical Skills
- Python
- Pandas
- Scikit-Learn
- K-Means Clustering
- Outlier Analysis
- Data Visualization
- Statistical Analysis
---
## Conclusion
Customer value is not evenly distributed across the customer base.
By combining RFM analysis, outlier detection, and customer segmentation, this project provides a practical framework for identifying valuable customers, reducing churn risk, and improving customer lifetime value.
The analysis shifts the conversation from:
> **"Who are our customers?"**
To:
> **"Which customers create the most value, which customers are at risk, and where should the business focus its retention efforts?"**
The resulting segmentation framework supports more informed marketing decisions, targeted retention initiatives, and a more effective allocation of customer engagement resources.
