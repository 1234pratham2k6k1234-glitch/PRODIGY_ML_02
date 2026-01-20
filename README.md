# 🛍️ Task 02 - Customer Segmentation using K-Means Clustering

## 📌 Overview
Customer segmentation is an important Machine Learning application in the retail industry.  
It helps businesses understand customer behavior, group customers into meaningful segments, and create better marketing strategies.

In this project, we use **K-Means Clustering (Unsupervised Learning)** to group customers based on their purchase-related behavior.

The final output provides customer clusters such as:
- High Income, High Spending customers (Premium customers)
- High Income, Low Spending customers (Potential customers)
- Low Income, High Spending customers (Deal seekers)
- Low Income, Low Spending customers (Budget customers)

---

## 🎯 Objective
To build a **K-Means clustering model** that groups retail store customers into different segments based on their purchase patterns.

---

## 📂 Dataset
Dataset used: **Mall Customers Dataset** (Kaggle)

The dataset includes customer details such as:
- Customer ID
- Gender
- Age
- Annual Income
- Spending Score

✅ Kaggle Dataset Link:  
https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

---

## ✅ Features Used for Clustering
For segmentation, the following two features are selected:

| Feature Name | Description |
|------------|-------------|
| **Annual Income (k$)** | Customer annual income |
| **Spending Score (1–100)** | Score assigned based on customer spending behavior |

These features are ideal for grouping customers into meaningful clusters.

---

## 🛠 Tools & Technologies Used
- **Python**
- **Pandas** (Data handling)
- **NumPy** (Numerical operations)
- **Matplotlib & Seaborn** (Visualization)
- **scikit-learn** (Clustering + Scaling + Evaluation)
- **Jupyter Notebook**

---

## 🔍 Project Workflow
### 1️⃣ Data Loading & Exploration
- Loaded the dataset using Pandas
- Checked dataset shape, columns, and null values

### 2️⃣ Feature Selection
- Selected `Annual Income (k$)` and `Spending Score (1-100)` as clustering inputs

### 3️⃣ Feature Scaling
K-means uses distance-based clustering, so scaling is required.  
We used **StandardScaler** to normalize the feature values.

### 4️⃣ Finding Optimal Number of Clusters (K)
To decide the best number of clusters, two methods were used:

✅ **Elbow Method**
- Plots WCSS (within-cluster sum of squares) for different K values  
- Best K is found at the "elbow point"

✅ **Silhouette Score**
- Measures how well-separated the clusters are
- Higher score indicates better clustering

### 5️⃣ Training K-Means Model
- Final K-Means model was trained using the selected optimal K
- Cluster labels were assigned to each customer

### 6️⃣ Visualization & Cluster Insights
- Plotted customer clusters using scatter plots
- Calculated average income and spending score per cluster for interpretation

### 7️⃣ Exporting Results
The clustered dataset was saved as:
✅ `clustered_customers.csv`

---

## 📊 Output
The notebook produces:
✅ Elbow graph to estimate optimal K  
✅ Silhouette score graph  
✅ Final clustered scatter plot  
✅ Cluster summary table (mean values per cluster)  
✅ Exported CSV with cluster labels  

---