# Starbucks Promotional Campaign Analysis and Customer Segmentation

## 🔎 Overview

This project analyzes a simulated Starbucks promotional campaign to **understand how customers respond to different marketing offers and identify meaningful customer segments.** By combining demographic data, promotional offer details, and transactional behavior, the analysis uncovers patterns in customer engagement, spending behavior, and offer effectiveness.

**Machine learning models and clustering techniques** are used to identify factors influencing offer completion and to segment customers into groups with distinct behaviors. The insights help businesses design more personalized and effective marketing campaigns.

## 🔐 Business Problem

Marketing campaigns often send the same promotions to a large customer base despite differences in demographics, purchasing behavior, and engagement levels. This can lead to:
- Low offer engagement
- Inefficient marketing spending
- Missed opportunities for personalized marketing

This project aims to answer the following questions:
- Which promotional offers are most effective?
- Which customer characteristics influence offer completion?
- How can customers be segmented to improve targeting strategies?

The goal is to develop insights that help businesses optimize promotional campaigns and improve customer targeting.
   
<img width="995" alt="Screenshot 2025-05-22 at 01 03 25" src="https://github.com/user-attachments/assets/5148dd85-ec68-488a-84a4-748b893f8b91" />

## 📊 Dataset

The dataset simulates Starbucks customer activity during a one-month promotional campaign and consists of three main tables, derived from [Kaggle](https://www.kaggle.com/datasets/ihormuliar/starbucks-customer-data).

### Portfolio (Offers)

Information about promotional offers sent to customers.

Features include:
- Offer type (BOGO, Discount, Informational)
- Reward amount
- Difficulty level
- Offer duration
- Promotional channels (email, mobile app, social media, web)

Dataset size: 10 offers × 6 attributes

### Profile (Customer Demographics)

Customer demographic information including:
- Age
- Gender
- Income
- Membership start date

Dataset size: ~17,000 customers

Most customers received 3–5 offers during the campaign, while some received none.

### Transcript (Customer Events)

Tracks customer interactions with offers and purchases.

Event types include:
- Offer received
- Offer viewed
- Offer completed
- Transactions

Dataset size: 306,000+ events

Each event includes a timestamp representing hours since the campaign began.

## 📍 Methodology

### 1. Data Preprocessing

- Cleaned missing values
- Converted data types
- Created additional features such as offer aliases
- Merged the datasets to create a unified analysis dataset

### 2. Exploratory Data Analysis

Explored patterns across:
- Customer demographics
- Offer characteristics
- Customer engagement with offers
- Transaction frequency and spending behavior

EDA helped identify offer performance trends and engagement patterns.

### 3. Predictive Modeling

Classification models were used to identify factors influencing offer completion:
- Logistic Regression
- Random Forest

Key predictors included:
- Customer age
- Income
- Offer reward
- Offer difficulty
- Promotional channels

### 4. Customer Segmentation

Customer groups were identified using:
- K-Means Clustering
- PCA (Principal Component Analysis)

Segmentation considered behavioral variables such as:
- Transaction frequency
- Total spending
- Offer engagement
- Offer completion rates

## 🔑 Key Insights

- Most Starbucks customers in the dataset are between 40 and 70 years old, with a peak around 50–60 years. Income levels mainly fall between $50,000 and $80,000, representing a middle-to-upper-middle income segment.
- BOGO and Discount offers are the most common promotions, while informational offers are less frequent. Offers typically last 5–7 days, with higher reward offers often requiring greater purchase difficulty.
- Transactions are the most frequent events, while offer viewing and completion occur less often. Engagement tends to spike periodically during the campaign, likely due to scheduled promotional releases.
- Most individual transactions are under $20, resulting in a highly skewed distribution. While most customers spend relatively small amounts overall, a small group of customers spends over $1,000, representing high-value customers.
- Five distinct customer segments were identified:
1. Low-Engagement Customers: Lowest transactions and offer completion rates.
2. High-Value Loyalists: High transaction counts, highest spending, and high offer engagement.
3. Low-Spend Infrequent Users: Low spending and low activity.
4. Affluent Moderates: Higher income customers with moderate engagement.
5. Frequent Low-Spenders: Frequent purchases but smaller transaction values.

## ✍️ Business Recommendations

### 1. Prioritize High-Value Loyalists

Strengthen loyalty through personalized promotions, exclusive rewards, and special offers during holidays or events.

### 2. Improve Engagement for Moderate Segments

Encourage more frequent visits through targeted offers, seasonal promotions, and personalized product recommendations.

### 3. Upsell Frequent Low-Spenders

Increase transaction value through cross-selling strategies such as discounts on pastries or premium drink upgrades.

### 4. Redesign Ineffective Offers

Offers with low view or completion rates should be adjusted by improving reward structures, simplifying requirements, or increasing promotional visibility.

### 5. Optimize Marketing Budget Allocation

Reduce marketing spend on consistently disengaged customers and allocate resources toward higher-return customer segments.

## ⚙ Tools & Techniques

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Machine Learning (Logistic Regression, Random Forest)
- Customer Segmentation (K-Means Clustering, PCA (Principal Component Analysis))
