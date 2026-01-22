# Two-Wheeler-Servicing-Customer-Clustering-Analysis
Segmented two-wheeler customers into Light, Moderate, and Heavy service groups using K-Means clustering on free and paid usage data to support efficient service planning and resource allocation.
# Two Wheeler Servicing – Customer Clustering Analysis

## 📌 Project Overview
This project focuses on segmenting two-wheeler customers based on their vehicle usage during **free** and **paid** servicing periods. Using **K-Means clustering**, customers are classified into **Light**, **Moderate**, and **Heavy** service requirement groups to support efficient service planning, manpower allocation, and operational decision-making.

The project demonstrates an **end-to-end data analytics workflow**, combining exploratory analysis, preprocessing, unsupervised learning, and business interpretation.

---

## 🏢 Business Problem
Two-wheeler service centers often treat all customers uniformly despite significant differences in riding behavior and servicing needs. This results in:
- Inefficient manpower utilization  
- Longer service turnaround times  
- Poor service capacity planning  

A data-driven customer segmentation approach is required to identify customers with varying service requirements and enable differentiated service strategies.

---

## 🎯 Business Objectives
- Segment customers based on **service usage intensity**
- Classify customers into:
  - **Light**
  - **Moderate**
  - **Heavy** service requirement groups
- Estimate servicing effort in terms of:
  - Time
  - Resources
  - Operational load
- Support **data-driven decisions** for service scheduling and manpower planning

---

## 📊 Dataset Description
- Source: **IIM Kozhikode (Case Study)**
- Total records: **18,590**
- Total variables: **20**
- Key variables used:
  - `FREE_AV_US` – Average usage during free servicing period
  - `PAID_AV_US` – Average usage during paid servicing period
  - `VISIT3`, `NUM_PAID_VIS` – Service progression indicators

---

## 🧭 Project Methodology

### Step 1: Exploratory Data Analysis (EDA)
- Dataset structure and variable inspection
- Missing value analysis
- Distribution analysis using histograms
- Outlier detection using boxplots
- Identification of natural usage patterns

### Step 2: Data Preprocessing
- Removal of records with missing usage values
- Sequential filtering:
  - `VISIT3 = 1`
  - `NUM_PAID_VIS = 2`
- Feature selection based on business relevance
- Standardization to prepare data for distance-based clustering

### Step 3: K-Means Clustering
- Elbow method used to identify optimal number of clusters
- Final selection: **K = 3**
- K-Means model applied to standardized data

### Step 4: Cluster Interpretation
- Cluster centroids transformed back to original scale
- Clusters labeled as:
  - **Light** – Low usage, minimal servicing needs
  - **Moderate** – Moderate usage, balanced servicing effort
  - **Heavy** – High usage, intensive servicing needs

### Step 5: Visualization & Business Insights
- Scatter plots used to visualize cluster separation
- Cluster-wise business interpretation
- Operational recommendations provided for each customer segment

---

## 📈 Key Results

| Customer Segment | Service Usage Pattern | Business Interpretation |
|-----------------|----------------------|-------------------------|
| Light | Low free & paid usage | Minimal servicing effort |
| Moderate | Medium free, high paid usage | Moderate servicing resources |
| Heavy | Very high free usage | High servicing effort & priority handling |

---

## 💡 Business Impact
- Enables differentiated service strategies
- Improves manpower and capacity planning
- Reduces service bottlenecks
- Enhances overall operational efficiency

---

## 🛠️ Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook


