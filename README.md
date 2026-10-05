# 📊 Product Segmentation using Hierarchical Clustering

## 📌 Project Overview

This project focuses on **Product Segmentation using Hierarchical Clustering**, an unsupervised machine learning technique.

The objective is to analyze product-related data and group similar products based on their **sales, order quantity, profit, shipping cost, and product base margin**. The analysis helps identify different product segments and provides useful insights for business and inventory management.

The project follows a complete data analysis and machine learning workflow, including **data preprocessing, outlier treatment, feature scaling, hierarchical clustering, dendrogram analysis, silhouette score evaluation, cluster analysis, and business insights**.

---

## 🎯 Objective

The main objective of this project is to identify meaningful groups of products using clustering techniques.

The analysis helps answer questions such as:

* Which products belong to similar groups?
* Which product segment generates higher sales?
* How do different product groups compare in terms of profit and order quantity?
* How can product segmentation support better business decisions?

---

## 📂 Dataset

The project uses an office-supply purchase dataset containing information about products, customers, sales, profit, shipping costs, and product margins.

The original dataset contains **5,977 observations**. After performing outlier treatment, **5,192 observations** were used for the final clustering analysis.

Some of the important variables are:

| Variable              | Description                  |
| --------------------- | ---------------------------- |
| `Products`            | Product name/category        |
| `Sales`               | Sales amount                 |
| `Order_Quan`          | Quantity of products ordered |
| `Profit`              | Profit generated             |
| `Shipping_Cost`       | Cost of shipping             |
| `Product_Base_Margin` | Product margin               |
| `Customer_Segment`    | Type of customer             |

---

## 🔍 Data Preprocessing

Before applying the clustering algorithm, the dataset was explored and prepared for analysis.

The project includes checking the dataset structure, data types, numerical variables, categorical variables, and unnecessary identifier columns.

### Outlier Treatment

Outliers were identified using **boxplots** and treated using the **IQR (Interquartile Range) method**.

After outlier treatment, the dataset was reduced from **5,977 to 5,192 observations**. This step helps reduce the influence of extreme values on the clustering algorithm.

### Missing Values

The dataset was also checked for missing values. No missing-value treatment was required for the final analysis.

---

## 📈 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the distribution and relationships between important variables.

The project uses visualizations such as:

* Boxplots for identifying outliers
* Product frequency analysis
* Cluster distribution plots
* Sales and profit visualizations

These visualizations help understand the dataset before applying machine learning.

---

## ⚙️ Feature Selection & Scaling

For clustering, the following numerical features were selected:

**Sales, Order Quantity, Profit, Shipping Cost, and Product Base Margin.**

Since these variables have different ranges, **StandardScaler** was applied to standardize the selected features.

Feature scaling is important because clustering algorithms use distance calculations, and variables with larger numerical ranges could otherwise have a greater influence on the model.

---

# 🤖 Hierarchical Clustering

## What is Hierarchical Clustering?

Hierarchical Clustering is an **unsupervised machine learning algorithm** used to group similar observations into clusters.

This project uses **Agglomerative Hierarchical Clustering**. In this approach, every observation initially starts as an individual cluster, and similar clusters are gradually merged together.

The project uses **Ward linkage**, which attempts to minimize the variance within each cluster.

---

## 🌳 Dendrogram

A **dendrogram** is used to visualize the hierarchical relationship between observations and clusters.

By analyzing the dendrogram, the project determines a suitable number of clusters for the final model.

The analysis indicates that **2 clusters** provide a meaningful segmentation of the products.

---

## 📊 Silhouette Score

The **Silhouette Score** is used to evaluate the quality of clustering.

It measures how similar an observation is to its own cluster compared with other clusters. A higher score generally indicates better-defined clusters.

Based on the analysis, **K = 2** was selected for the final clustering model.

### Model Summary

| Parameter              | Result                                |
| ---------------------- | ------------------------------------- |
| Algorithm              | Agglomerative Hierarchical Clustering |
| Linkage                | Ward                                  |
| Optimal Clusters       | 2                                     |
| Cophenetic Correlation | 0.7772                                |

---

# 🧩 Cluster Analysis

After applying the clustering algorithm, two major product groups were identified.

### Cluster 0 — Technology

The first cluster contains a large number of technical products. The major products include **Telephones and Communication, Vending Machines, Computer Peripherals, Air Conditioners, Copiers and Fax, and Office Machines**.

Based on the dominant product types, this cluster was classified as **Technology**.

The cluster has an average sales value of approximately **$8,854** and an average order quantity of around **33**.

### Cluster 1 — Stationary

The second cluster mainly contains stationery-related products such as **Paper, Binders and Binder Accessories, Pens and Art Supplies, Labels, Rubber Bands, and Envelopes**.

Therefore, this cluster was classified as **Stationary**.

The cluster has an average sales value of approximately **$635** and an average order quantity of around **25**.

### Cluster Comparison

| Metric                 | Technology | Stationary |
| ---------------------- | ---------: | ---------: |
| Number of Observations |      1,733 |      3,459 |
| Average Sales          |  $8,854.20 |    $634.82 |
| Average Order Quantity |         33 |         25 |
| Average Profit         |  $2,513.39 |     $71.19 |

The comparison shows that the **Technology cluster has considerably higher average sales and profit**, while the Stationary cluster contains more observations.

---

# 📊 Visualizations

The project includes several visualizations to understand the data and clustering results:

### 1. Outlier Analysis

Boxplots are used to identify extreme values in numerical variables.

### 2. Dendrogram

The dendrogram shows the hierarchical relationship between different observations and helps determine the number of clusters.

### 3. Silhouette Score

The Silhouette Score visualization helps evaluate different cluster configurations.

### 4. Cluster Distribution

A visualization is used to compare the number of observations belonging to each cluster.

### 5. Cluster Visualization

The final clusters are visualized to understand the separation between the identified product groups.

---

# 💡 Business Insights

The clustering analysis provides several useful business insights.

The **Technology segment** has significantly higher average sales and profit compared with the Stationary segment. This indicates that technology-related products contribute more strongly to the business in terms of average financial performance.

Although the Stationary cluster contains more observations, its average sales and profit are considerably lower.

The company can use these insights for:

* Inventory planning
* Product-level sales analysis
* Stock management
* Identifying high-performing product groups
* Business strategy and decision-making

---

# 📁 Project Structure

```text
Product-Segmentation-Hierarchical-Clustering/
│
├── 2_USL_Faculty_Notebook.ipynb
├── purchase.xlsx
├── README.md
│
└── images/
    ├── outlier_analysis.png
    ├── dendrogram.png
    ├── silhouette_score.png
    ├── cluster_distribution.png
    └── cluster_visualization.png
```

---

# 🚀 How to Run

1. Clone or download this repository.
2. Open `2_USL_Faculty_Notebook.ipynb` using Jupyter Notebook or Google Colab.
3. Keep the `purchase.xlsx` dataset in the same project folder.
4. Install the required Python libraries.
5. Run the notebook cells sequentially.

---

# 🧠 Skills Demonstrated

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Data Cleaning
* Exploratory Data Analysis
* Outlier Treatment
* Feature Scaling
* Data Visualization
* Hierarchical Clustering
* Agglomerative Clustering
* Dendrogram
* Silhouette Score
* Business Insight Generation

---

# ✅ Conclusion

This project demonstrates the use of **Hierarchical Clustering for product segmentation**.

By analyzing sales, order quantity, profit, shipping cost, and product margin, the project identifies two major product groups: **Technology** and **Stationary**.

The analysis shows that Technology products have much higher average sales and profit. These findings can help businesses understand product performance and make better **data-driven decisions related to inventory, sales, and product management**.
