# Customer Segmentation and Market Basket Analysis
### CS 4412 – Data Mining  
# CS4412 Retail Analysis Project (M3)

## Project Overview
This project analyzes customer purchasing behavior using the UCI Online Retail dataset.  
The goal is to discover meaningful patterns in customer transactions and support business decisions such as customer segmentation, cross-selling, and anomaly detection.

This milestone (M3) represents a **complete implementation** of the data mining pipeline, including feature engineering, clustering, classification, and anomaly detection.


## Discovery Questions

1. **Which products are frequently purchased together?**  
   → Addressed using association rule mining (Apriori)

2. **Are there natural customer segments based on purchasing behavior?**  
   → Addressed using RFM, K-Means (original + PCA), Decision Tree, Naive Bayes.
     four segments were identified (VIP, loyal, regular, inactive). 
     Frequency and Monetary define high-value customers, while Recency identifies inactive ones.

3. **Are there anomalous customers or transactions?**  
   → Addressed using Isolation Forest and Local Outlier Factor (LOF)
     anomalies include high-spending and high-frequency customers (likely wholesale or special cases), consistently detected across methods.


##  Implementation Pipeline

The analysis follows a structured data mining workflow:

1. **Data Cleaning**
   - Removed missing values
   - Filtered negative quantities and prices
   - Removed return transactions (InvoiceNo starting with 'C')

2. **Feature Engineering (RFM)**
   - Recency: Days since last purchase
   - Frequency: Number of transactions
   - Monetary: Total spending

3. **Clustering**
   - K-Means applied on original RFM features
   - PCA applied as preprocessing to improve clustering
   - Comparison between original vs PCA-based clustering

4. **Decision Tree (Interpretability)**
   - Used to explain cluster structure
   - Identifies key features distinguishing customer segments

5. **Naive Bayes (Discovery) and PCA visualization**
   - Analyzes conditional probabilities of features given clusters
   - Provides interpretable insights into customer behavior
   

6. **Anomaly Detection**
   - Isolation Forest and LOF used to identify unusual customers
   - Detects high-value outliers and rare purchasing patterns


## Key Results

- Identified **four distinct customer segments**:
  - Elite customers (high frequency, high spending)
  - Loyal high-value customers
  - Regular mid-value customers
  - Low-value / inactive customers

- Naive Bayes reveals strong relationships between:
  - High Frequency & Monetary → VIP customers
  - High Recency → inactive customers

- Anomaly detection highlights:
  - High-spending wholesale-like customers
  - Extreme purchasing behavior

## Visualization

The project includes multiple visualization layers:

- RFM pairwise scatter plots (local interpretation)
- PCA-based clustering visualization (global structure)
- Naive Bayes probability heatmaps
- Anomaly detection plots


## Current Status (M3)

✔ Complete data pipeline  
✔ All techniques implemented and working  
✔ Meaningful patterns discovered  
✔ Discovery questions largely answered  

The project is **functionally complete**. Remaining work focuses on refinement and presentation.


## Plan for M4

- Improve visualization quality and layout
- Enhance interpretation and storytelling
- Evaluate model limitations and robustness
- Finalize report for portfolio-level quality

##  Technologies Used

- Python (Pandas, NumPy)
- Scikit-learn (KMeans, PCA, Decision Tree, Naive Bayes)
- Seaborn & Matplotlib
- MLxtend (Apriori)

##  Repository Structure
CS4412_Project_Jia_Liu/
data/
    raw/
    Online Retail .xlsx
notebook/
    M1_Proposal.ipynb
    M2_Initial_Implementation.ipynb
    M3_Complete_Implementation.ipynb
docs/
    CS4412_JIA_LIU_M3.pdf
    M1-Proposal.pdf
    M2-Initial Implementation.pdf
figures/
src/
       

## Author
Jia Liu  
CS 4412 – Data Mining  
Kennesaw State University
