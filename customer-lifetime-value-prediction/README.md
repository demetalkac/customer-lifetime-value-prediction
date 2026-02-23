{\rtf1\ansi\ansicpg1254\cocoartf2639
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 AppleColorEmoji;\f2\fnil\fcharset0 LucidaGrande;
}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-XGBoost-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

\f0\fs24 \cf0 # End-to-End Customer Analytics & Predictive Modeling\
\
## 
\f1 \uc0\u55357 \u56524 
\f0  Project Overview\
\
This project demonstrates an end-to-end customer analytics pipeline, including:\
\
- RFM segmentation\
- K-Means clustering\
- Probabilistic Customer Lifetime Value (CLV) modeling\
- Leakage-aware time-based predictive modeling using XGBoost\
\
The objective is to identify and predict high-value customers using both analytical segmentation and machine learning techniques.\
\
---\
\
## 
\f1 \uc0\u55356 \u57263 
\f0  Business Problem\
\
Companies need to:\
\
- Identify high-value customers\
- Predict future customer value\
- Allocate marketing budget efficiently\
- Reduce churn risk\
\
This project simulates a real-world CRM analytics workflow to address these needs.\
\
---\
\
## 
\f1 \uc0\u55357 \u56522 
\f0  Dataset\
\
The dataset consists of transactional e-commerce data including:\
\
- InvoiceNo\
- StockCode\
- Description\
- Quantity\
- InvoiceDate\
- UnitPrice\
- CustomerID\
- Country\
\
Revenue was engineered as:\
\
Revenue = Quantity \'d7 UnitPrice\
\
---\
\
## 
\f1 \uc0\u55358 \u56825 
\f0  Data Cleaning\
\
- Removed cancelled transactions\
- Filtered negative quantities and prices\
- Handled missing CustomerID values\
- Created revenue column\
- Converted InvoiceDate to datetime\
\
---\
\
## 
\f1 \uc0\u55357 \u56589 
\f0  
\f1 1\uc0\u65039 \u8419 
\f0  RFM Segmentation\
\
Calculated:\
\
- Recency\
- Frequency\
- Monetary\
\
Customers were segmented into:\
\
- Champions\
- Loyal Customers\
- At Risk\
- Potential\
- Lost\
\
---\
\
## 
\f1 \uc0\u55358 \u56598 
\f0  
\f1 2\uc0\u65039 \u8419 
\f0  K-Means Clustering\
\
Applied K-Means clustering to validate natural customer groupings.\
\
- Used log transformation\
- Standard scaling\
- Evaluated with Elbow & Silhouette methods\
\
---\
\
## 
\f1 \uc0\u55357 \u56496 
\f0  
\f1 3\uc0\u65039 \u8419 
\f0  Probabilistic CLV Modeling\
\
Used:\
\
- BG/NBD model 
\f2 \uc0\u8594 
\f0  future purchase prediction\
- Gamma-Gamma model 
\f2 \uc0\u8594 
\f0  expected average order value\
\
Estimated:\
\
- 6-month CLV\
- 12-month CLV\
\
Segment-level CLV insights were analyzed.\
\
---\
\
## 
\f1 \uc0\u9888 \u65039 
\f0  Baseline ML Model\
\
A classification model was initially trained using CLV-based labels.\
\
However, high ROC AUC (~0.98) indicated potential target leakage due to same-period modeling.\
\
---\
\
## 
\f1 \uc0\u55357 \u56960 
\f0  
\f1 4\uc0\u65039 \u8419 
\f0  Time-Based Predictive Modeling (Leakage-Free)\
\
To avoid leakage:\
\
- Defined a cutoff date\
- Generated features only from historical (pre-cutoff) data\
- Created target using future 90-day revenue\
- Applied time-based validation\
\
### Model\
\
XGBoost Classifier\
\
### Performance\
\
- Accuracy: 0.73\
- ROC AUC: 0.82\
- PR AUC: 0.81\
\
Top predictive features:\
\
- total_orders\
- unique_invoices\
- total_quantity\
- max_basket\
\
This model realistically predicts future high-value customers.\
\
---\
\
## 
\f1 \uc0\u55358 \u56800 
\f0  Key Insights\
\
- Purchase frequency and transaction volume strongly predict future value\
- Champions remain the most valuable segment in both historical and predictive analyses\
- Time-based validation significantly reduces over-optimistic performance\
\
---\
\
## 
\f1 \uc0\u55357 \u57056 
\f0  Technologies Used\
\
- Python\
- Pandas\
- NumPy\
- Scikit-learn\
- XGBoost\
- Lifetimes (BG/NBD & Gamma-Gamma)\
- Matplotlib\
\
---\
\
## 
\f1 \uc0\u55357 \u56520 
\f0  Future Improvements\
\
- Hyperparameter tuning\
- SHAP-based explainability\
- Threshold optimization for marketing ROI\
- Production-ready pipeline\
\
---\
\
## 
\f1 \uc0\u55356 \u57235 
\f0  Author\
\
This project was developed as part of advanced customer analytics and predictive modeling practice.\
}