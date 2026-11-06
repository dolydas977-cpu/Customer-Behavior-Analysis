# Customer Shopping Behavior Analysis

An end-to-end data analysis project that studies **3,900 customer purchases** to understand spending patterns, customer segments, product preferences and subscription behavior, and to guide business decisions.

**Tools used:** Python (pandas) · PostgreSQL · SQL · Power BI

---

## Project Overview

This project analyses transactional shopping data across several product categories. The goal is to answer practical business questions, such as:

- Who generates the most revenue?
- Which products do customers rate highest?
- Do subscribers, express-shipping users or discount users behave differently?
- How loyal is the customer base?

## Dataset Summary

| Item | Detail |
|---|---|
| Rows | 3,900 purchases |
| Columns | 18 |
| Missing data | 37 values in the `Review Rating` column |

**Key features**
- **Customer demographics:** Age, Gender, Location, Subscription Status
- **Purchase details:** Item Purchased, Category, Purchase Amount, Size, Colour
- **Shopping behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

## Workflow

### 1. Data preparation in Python
- **Data loading:** imported the dataset with pandas.
- **Initial exploration:** used `df.info()` and `df.describe()` to check structure and summary statistics.
- **Missing data:** filled missing `Review Rating` values using the median rating of each product category.
- **Column standardization:** renamed columns to snake case for readability.
- **Feature engineering:** created `age_group` (age bins) and `purchase_frequency_days`.
- **Consistency check:** found that `discount_applied` and `promo_code_used` were redundant, so `promo_code_used` was dropped.
- **Database integration:** loaded the cleaned DataFrame into PostgreSQL for SQL analysis.

### 2. Business analysis in PostgreSQL
Ten business questions were answered with SQL:

1. Revenue by gender
2. High-spending discount users
3. Top 5 products by average rating
4. Shipping type comparison (Standard vs Express)
5. Subscribers vs non-subscribers
6. Discount-dependent products
7. Customer segmentation (New, Returning, Loyal)
8. Top 3 products per category
9. Repeat buyers and subscriptions
10. Revenue by age group

### 3. Dashboard in Power BI
An interactive dashboard presents the results visually, with filters for subscription status, gender, category and shipping type.

<img width="628" height="338" alt="Screenshot 2026-11-06 151226" src="https://github.com/user-attachments/assets/d03b178b-80d9-46aa-be70-3fef361a2251" />



## Key Insights

| Topic | Finding |
|---|---|
| **Revenue by gender** | Male customers generated **$157,890 (68%)** vs **$75,191 (32%)** from female customers. |
| **Revenue by age group** | Young adults lead with **$62,143**, followed by middle age ($59,197), adult ($55,978) and senior ($55,763). |
| **High-value discount users** | **839 customers** used a discount and still spent above the average purchase amount. |
| **Top-rated products** | Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80) and Skirt (3.78). |
| **Discount-dependent products** | Hat (50%), Sneakers (49%), Coat (49%), Sweater (48%) and Pants (47%) have the highest share of discounted purchases. |
| **Shipping** | Express orders average **$60.48** vs **$58.46** for Standard (about 3.5% higher). |
| **Subscriptions** | **1,053** subscribers produced **$62,645** in revenue. Average spend is almost the same: $59.49 (subscribers) vs $59.87 (non-subscribers). |
| **Repeat buyers** | 958 subscribers and 2,518 non-subscribers are repeat buyers (more than 5 purchases). |
| **Customer segments** | **Loyal:** 3,116 (80%) · **Returning:** 701 (18%) · **New:** 83 (2%) |
| **Top products per category** | Jewelry (Accessories), Blouse (Clothing), Sandals (Footwear), Jacket (Outerwear). |

**Dashboard headline numbers:** 3.9K customers · $59.76 average purchase amount · 3.75 average review rating.

## Business Recommendations

- **Boost subscriptions:** promote exclusive benefits for subscribers.
- **Customer loyalty programs:** reward repeat buyers and keep them in the "Loyal" segment.
- **Review discount policy:** balance sales boosts with margin control.
- **Product positioning:** highlight top-rated and best-selling products in campaigns.
- **Targeted marketing:** focus on high-revenue age groups and express-shipping users.

## Repository Structure

```
├── README.md
├── data/                  # dataset (CSV)
├── notebooks/             # Python notebook (data cleaning and EDA)
├── sql/                   # SQL queries
├── dashboard/             # Power BI file (.pbix)
├── images/                # dashboard screenshot
└── presentation/          # PowerPoint summary
```

> Adjust the folder names above to match the files you upload.

## How to Run

1. Clone this repository.
2. Install the Python libraries: `pip install pandas sqlalchemy psycopg2-binary`
3. Run the notebook to clean the data and load it into PostgreSQL.
4. Run the SQL queries in PostgreSQL (pgAdmin or any SQL client).
5. Open the `.pbix` file in Power BI Desktop to explore the dashboard.

## About Me

**Doly Das** — Assistant Manager with about 8 years of experience in credit risk, asset quality and MIS reporting. Skilled in Advanced Excel, Power BI, SQL and Python.

- GitHub: [dolydas977-cpu](https://github.com/dolydas977-cpu)
- LinkedIn: [add your LinkedIn link here](https://www.linkedin.com/in/your-name)

