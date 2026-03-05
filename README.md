# Customer Segmentation and Market Basket Analysis in Online Retail Data

## 1. Project Overview
This project analyzes retail transaction data to discover hidden patterns in customer purchasing behavior. Using the UCI Online Retail dataset, the project explores product associations and customer transaction patterns through data mining techniques.
The main goal is to identify meaningful patterns that can support marketing strategies, product bundling, and business decision-making.

## 2. Dataset
The dataset used in this project is the **Online Retail Dataset** from the **UCI Machine Learning Repository**.
Dataset information:
- Size: 22.6 MB
- Records: 541,909 transactions
- Attributes: 8 variables

Key attributes include:

| Attribute | Description |
|-----------|-------------|
| InvoiceNo | Transaction ID |
| StockCode | Product ID |
| Description | Product name |
| Quantity | Number of items purchased |
| InvoiceDate | Date of transaction |
| UnitPrice | Price per product |
| CustomerID | Customer identifier |
| Country | Customer country |

Dataset source:  
https://archive.ics.uci.edu/ml/datasets/online+retail


## 3. Project Objectives
This project focuses on the following discovery questions:
- What products are frequently purchased together?
- Are there meaningful patterns in retail transactions?
- How can association rules help understand customer purchasing behavior?

## 5. Key Findings (M2 Initial Implementation)
Preliminary association rule mining reveals several product co-purchase patterns. For example:
- Certain decorative items and gift-related products frequently appear together in transactions.
- Seasonal and themed products often form strong associations.

These findings suggest opportunities for **product bundling and cross-selling strategies** in online retail environments.


## 8. Future Work (M3 Plan)
The next stage of the project will include:
- Customer segmentation using clustering algorithms (K-Means or DBSCAN)
- Anomaly detection in transaction data
- Further evaluation of discovered patterns

## 9. Author
Jia Liu  
CS 4412 – Data Mining  
Kennesaw State University
