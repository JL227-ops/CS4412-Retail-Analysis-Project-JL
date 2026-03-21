# Customer Segmentation and Market Basket Analysis
### CS 4412 – Data Mining  

# Project Overview
This project analyzes customer transaction data from the **UCI Online Retail dataset** in order to discover patterns in purchasing behavior.
The project applies several data mining techniques, including:
- Exploratory Data Analysis (EDA)
- Data preprocessing and cleaning
- Association Rule Mining (Apriori)
- Customer segmentation using clustering

The goal is to identify meaningful relationships between products and understand customer purchasing patterns that could support data-driven marketing strategies.
---

# Dataset
The dataset used in this project is the **Online Retail Dataset** from the UCI Machine Learning Repository.

Dataset characteristics:

- **Rows:** 541,909
- **Attributes:** 8
- **Format:** Excel (.xlsx)
- **Time range:** 2010–2011
- **Business type:** UK-based online retailer

Each row represents a purchased product within a transaction.

### Features

| Feature | Description |
|------|------|
| InvoiceNo | Transaction identifier |
| StockCode | Product identifier |
| Description | Product name |
| Quantity | Number of items purchased |
| InvoiceDate | Date and time of purchase |
| UnitPrice | Price per item |
| CustomerID | Unique customer ID |
| Country | Customer location |

---
# Project Structure


---

# Data Preprocessing
Several preprocessing steps were applied to improve data quality before performing mining tasks.
Key preprocessing decisions include:
1. **Removing missing values**
Rows containing missing values were removed to ensure valid transaction records.
2. **Filtering product returns**
Transactions with negative quantities were removed because they represent product returns rather than purchases.
3. **Removing invalid prices**
Rows with zero or negative prices were filtered out.
4. **Feature engineering**
A new feature called **TotalPrice** was created:

TotalPrice = Quantity × UnitPrice
This represents the total value of a purchased item.
---
# Exploratory Data Analysis
Exploratory analysis was performed to understand the structure and characteristics of the dataset.
Key observations include:
- Purchase quantities follow a **long-tailed distribution**
- Most transactions involve **small purchase quantities**
- The majority of customers are located in the **United Kingdom**
- Unit prices are generally **low with several outliers**

Several visualizations were created to illustrate these patterns.
Example visualizations include:
- Quantity distribution histogram
- Price vs quantity scatter plot
- Country distribution
- Correlation heatmap
- K-Means clustering visualization
---

# Association Rule Mining
Association rule mining was applied using the **Apriori algorithm** to identify products that are frequently purchased together.
The dataset was converted into a transactional format where each invoice represents a basket of purchased items.
Association rules were evaluated using the following metrics:
| Metric | Description |
|------|------|
| Support | Frequency of the itemset |
| Confidence | Probability of purchasing B given A |
| Lift | Strength of association compared to random |
Rules with lift greater than 1 indicate meaningful relationships between products.
These patterns may help retailers design strategies such as:
- Product bundling
- Cross-selling
- Recommendation systems
---

# Initial Clustering Results
Customer behavior patterns were explored using **K-Means clustering**.
Transactions were aggregated at the invoice level using:
- Total quantity purchased
- Average unit price

After scaling the data, K-Means clustering was applied to identify groups of transactions with similar purchasing characteristics.
The resulting clusters suggest different purchasing behaviors, such as:
- Small frequent purchases
- Large bulk purchases
- Higher price transactions
---

# Results and Insights
The initial analysis reveals that the dataset contains meaningful patterns in customer transactions.
Key insights include:
- Some products frequently appear together within the same transaction
- Retail transactions follow a typical long-tail distribution

These insights demonstrate the potential of data mining techniques for discovering actionable patterns in retail datasets.

---

# Milestone 3 Plan
The next stage of the project will extend the analysis by applying additional data mining techniques.
Planned tasks include:
- Customer segmentation using **K-Means and DBSCAN**
- Anomaly detection using **Isolation Forest**
- Identifying unusual transactions or customers
- Further analysis of purchasing patterns
These methods will provide deeper insights into customer behavior.
---

# Technologies Used
The project was implemented using Python and common data science libraries.
Main libraries include:
pandas
numpy
matplotlib
seaborn
scikit-learn
mlxtend
openpyxl

# Installation
Install dependencies:
pip install -r requirements.txt

# Running the Notebook
Open the main notebook:
notebooks/M2_Initial_Implemntation.ipynb


The notebook contains:
- Data loading
- Data preprocessing
- EDA visualizations
- Association rule mining


---

# Author

Jia Liu  
CS 4412 – Data Mining  
Kennesaw State University

## 7. Author
Jia Liu  
CS 4412 – Data Mining  
Kennesaw State University
