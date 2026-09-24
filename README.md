# 🛍️ Customer Shopping Behavior Analysis

An end-to-end **Data Analytics project** focused on understanding customer purchasing behavior, identifying business trends, and generating actionable insights using **Python, SQL, and Power BI**.

The project follows a complete analytics workflow — from raw data exploration and cleaning to SQL-based analysis, interactive dashboard development, reporting, and business presentation.

---

## 📌 Overview

The objective of this project is to analyze customer shopping behavior and answer important business questions related to:

* Customer purchasing patterns
* Product and category performance
* Customer segmentation
* Discounts and purchasing behavior
* Sales and revenue trends
* Customer loyalty and repeat purchases
* Factors influencing purchasing decisions

The project demonstrates how raw customer data can be transformed into meaningful business insights using multiple data analytics tools.

### 🔄 End-to-End Workflow

**Raw Dataset → Python → EDA → Data Cleaning → PostgreSQL → SQL Analysis → Power BI → Report → Presentation**

---

## 📂 Dataset

The project uses a **Customer Shopping Behavior** dataset containing customer-level purchasing information.

### Dataset includes information related to:

* Customer demographics
* Item purchased
* Category
* Purchase amount
* Discount applied
* Previous purchases
* Purchase frequency
* Customer behavior
* Other purchasing-related attributes

The original dataset is available in the repository:

`customer_shopping_behavior.csv`

---

## 🛠️ Tools & Technologies

| Tool / Technology        | Purpose                                     |
| ------------------------ | ------------------------------------------- |
| **Python**               | Data loading, exploration and preprocessing |
| **Pandas**               | Data manipulation and cleaning              |
| **NumPy**                | Numerical analysis                          |
| **Matplotlib / Seaborn** | Exploratory data visualization              |
| **PostgreSQL**           | SQL-based business analysis                 |
| **SQL**                  | Data querying and business problem solving  |
| **Power BI**             | Interactive dashboard development           |
| **Gamma**                | Business presentation                       |
| **GitHub**               | Project version control and documentation   |

---

# 🔎 Project Workflow

## 1. Data Loading in Python

The customer shopping dataset was first loaded into Python using **Pandas**.

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")

print(df.head())
print(df.shape)
print(df.info())
```

The initial analysis focused on understanding:

* Dataset dimensions
* Column names
* Data types
* Missing values
* Duplicate records
* Basic statistics

---

## 2. Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to understand the structure and behavior of the dataset.

### Key EDA activities

* Dataset overview
* Descriptive statistics
* Missing-value analysis
* Duplicate detection
* Numerical variable analysis
* Categorical variable analysis
* Distribution analysis
* Relationship analysis
* Identifying patterns and anomalies

Example:

```python
df.describe()
df.isnull().sum()
df.duplicated().sum()
```

EDA helped identify potential data-quality issues and provided an initial understanding of customer behavior.

---

## 3. Data Cleaning & Preparation

The dataset was cleaned and prepared for further analysis.

### Cleaning activities included:

* Handling missing values
* Checking duplicate records
* Correcting data types
* Standardizing categorical values
* Reviewing inconsistent data
* Preparing analytical columns
* Validating the cleaned dataset

The cleaned data was then prepared for SQL analysis and Power BI visualization.

---

# 🗄️ 4. SQL Analysis

The cleaned dataset was loaded into **PostgreSQL** for structured business analysis.

SQL queries were written to answer practical business questions and identify customer and product-level insights.

### Analysis included:

* Customer segmentation
* Product performance
* Category-level analysis
* Discount analysis
* Purchase behavior
* Customer loyalty
* Previous purchase analysis
* Sales and purchase trends
* High-value customer analysis

### Example SQL Query

```sql
SELECT 
    item_purchased,
    ROUND(
        SUM(
            CASE 
                WHEN discount_applied = 'Yes' THEN 1 
                ELSE 0 
            END
        ) * 100.0 / COUNT(*),
        2
    ) AS discount_rate
FROM customer
GROUP BY item_purchased
ORDER BY discount_rate DESC
LIMIT 5;
```

The SQL analysis is available in:

`customer_behaviour.sql`

---

# 📊 5. Power BI Dashboard

The analyzed data was used to build an interactive **Power BI dashboard**.

The dashboard provides a visual overview of customer shopping behavior and enables users to explore different business dimensions.

### Dashboard components include:

* KPI cards
* Customer analysis
* Product analysis
* Category performance
* Purchase behavior
* Discount analysis
* Customer segmentation
* Interactive filters and slicers
* Business performance visualizations

Power BI file:

`customer_behavior.pbix`

---

# 📈 6. Results & Insights

The analysis helped identify meaningful patterns in customer shopping behavior.

### Key areas of insight

**Customer Behavior**

* Understanding how customers purchase and interact with products.
* Identifying differences between customer segments.

**Product & Category Performance**

* Identifying products and categories with stronger purchasing activity.
* Comparing performance across different categories.

**Discount Analysis**

* Understanding the relationship between discounts and purchases.
* Identifying products with higher discount usage.

**Customer Segmentation**

* Categorizing customers based on their previous purchase behavior.
* Identifying returning and loyal customer groups.

**Business Analysis**

* Translating SQL findings into business-focused insights.
* Supporting data-driven decision-making through dashboard visualization.

> Detailed numerical findings and recommendations are available in the project report.

---

# 📄 7. Business Problem Document

A separate **Business Problem Document** was created to define the business context and analytical requirements before performing the analysis.

File:

`Business Problem Document.pdf`

This document helps connect the technical analysis with actual business questions.

---

# 📝 8. Project Report

A detailed project report was prepared covering the complete analytical process.

The report includes:

1. Business problem
2. Dataset overview
3. Data preparation
4. Exploratory Data Analysis
5. SQL analysis
6. Power BI dashboard
7. Key findings
8. Business insights
9. Recommendations
10. Conclusion

File:

`Customer Shopping Behavior Analysis.pdf`

---

# 🎤 9. Presentation

The project findings were converted into a professional presentation using **Gamma**.

The presentation focuses on communicating the analysis in a clear, business-friendly manner.

### Presentation covers:

* Business problem
* Dataset
* Analytical approach
* Data preparation
* SQL analysis
* Power BI dashboard
* Key insights
* Recommendations
* Conclusion

File:

`Customer-Shopping-Behavior-Analysis-ppt.pptx`

---

# 📁 Repository Structure

```text
customer_behavior_analysis/
│
├── customer_shopping_behavior.csv
│
├── Customer_Shopping_Behavior_Analysis.ipynb
│
├── customer_behaviour.sql
│
├── customer_behavior.pbix
│
├── Business Problem Document.pdf
│
├── Customer Shopping Behavior Analysis.pdf
│
├── Customer-Shopping-Behavior-Analysis-ppt.pptx
│
└── README.md
```

---

# ▶️ How to Run

## Step 1 — Clone the Repository

```bash
git clone https://github.com/Yashlawaniya/customer_behavior_analysis.git
```

Navigate to the project folder:

```bash
cd customer_behavior_analysis
```

---

## Step 2 — Install Python Libraries

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

## Step 3 — Run the Python Notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Customer_Shopping_Behavior_Analysis.ipynb
```

Run the notebook cells sequentially to perform:

* Data loading
* EDA
* Data cleaning
* Data preparation

---

## Step 4 — Perform SQL Analysis

Set up a PostgreSQL database and import the cleaned customer data.

Open:

```text
customer_behaviour.sql
```

Execute the queries to reproduce the business analysis.

---

## Step 5 — Open the Power BI Dashboard

Open:

```text
customer_behavior.pbix
```

using **Power BI Desktop**.

If required, update the database/data-source connection before refreshing the dashboard.

---

## Step 6 — Review the Report

Open:

```text
Customer Shopping Behavior Analysis.pdf
```

to review the complete analytical findings and recommendations.

---

## Step 7 — View the Presentation

Open:

```text
Customer-Shopping-Behavior-Analysis-ppt.pptx
```

to view the project presentation created using **Gamma**.

---

# 💡 Skills Demonstrated

### Data Analytics

* Exploratory Data Analysis
* Data Cleaning
* Data Preprocessing
* Business Analysis
* Customer Behavior Analysis

### Python

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn

### SQL

* PostgreSQL
* SELECT statements
* WHERE conditions
* GROUP BY
* ORDER BY
* CASE statements
* Aggregate functions
* Subqueries
* CTEs
* Business-oriented SQL analysis

### Business Intelligence

* Power BI
* KPI Development
* Data Visualization
* Dashboard Design
* Interactive Filtering
* Data Storytelling

### Reporting & Communication

* Business Problem Definition
* Analytical Reporting
* Business Insights
* Recommendations
* Presentation Development
* Gamma

---

# 🔗 Project Links

### 📂 GitHub Repository

[Customer Behavior Analysis — GitHub Repository](https://github.com/Yashlawaniya/customer_behavior_analysis)

### 👨‍💻 GitHub Profile

[Yash Lawaniya — GitHub](https://github.com/Yashlawaniya)

### 💼 LinkedIn

[Yash Lawaniya — LinkedIn](https://www.linkedin.com/in/yashlawaniya/)

---

# 👤 Author

## Yash Lawaniya

**B.Tech — Computer Science & Engineering**

Aspiring **Business Analyst | Data Analyst | Project Coordinator**

📍 India

🔗 [GitHub](https://github.com/Yashlawaniya)
🔗 [LinkedIn](https://www.linkedin.com/in/yashlawaniya/)

---

## ⭐ Project Summary

**Customer Shopping Behavior Analysis** is an end-to-end data analytics project demonstrating the ability to work with data across the complete analytics lifecycle — from **Python-based data exploration and cleaning to PostgreSQL analysis, Power BI dashboard development, business reporting, and presentation**.

The project focuses not only on technical data analysis but also on converting analytical findings into **clear business insights and actionable recommendations**.
