# 🛒 Product Placement Optimization using Machine Learning Clustering

This project uses unsupervised machine learning techniques to optimize in-store product placement based on customer transaction data. By clustering customer purchasing behavior, we recommend optimal shelf placement to enhance store navigation, sales, and customer satisfaction.

---

## 📁 Dataset

**Supermart Grocery Sales – Retail Analytics Dataset**  
Contains details such as:
- Product Category  
- Quantity  
- Unit Price  
- Total Spend  
- Tax  
- Customer Ratings  

---

## 📊 Machine Learning Models Used

We used three clustering models for customer segmentation:

1. **K-Means Clustering**  
   - Fast, efficient partitioning into `k` clusters.
   - Minimizes variance within clusters.

2. **Hierarchical Clustering**  
   - Builds nested clusters (tree/dendrogram).
   - Good for discovering hierarchy in data.

3. **DBSCAN (Density-Based Spatial Clustering)**  
   - Finds clusters based on density.
   - Can identify outliers (noise points) and does not require predefining `k`.

---

## 📐 Preprocessing Steps

- Missing value handling using **forward fill**.
- Categorical encoding of `Product_Category` via **Label Encoding**.
- **Standardization** of numeric features using `StandardScaler`.
- **PCA (Principal Component Analysis)** to reduce dimensionality before clustering.

---

## 📈 Evaluation Metrics

| Metric              | Description                                                   | Ideal Value |
|---------------------|---------------------------------------------------------------|-------------|
| **Silhouette Score**| How well a point fits in its cluster vs. others               | Higher      |
| **Davies-Bouldin**  | Ratio of within-cluster to between-cluster distance           | Lower       |

---

## 🧭 Store Layout Recommendation

Based on the clustering output, product categories are sorted by frequency across clusters and mapped to logical store zones like:

Entrance: Most frequently bought item
Middle Aisle: High-frequency essentials
Back Aisle: Less frequent staples
Checkout Area: Impulse-buy items
Side Aisles: Other grouped categories


This layout strategy improves navigation and maximizes conversion.

---

## 📊 Visualizations

- Cluster **scatterplots** (via PCA)
- Product frequency **heatmaps**
- Product placement **bar plots** by cluster

---

## ✅ Results

| Model        | Silhouette Score | Davies-Bouldin Index |
|--------------|------------------|-----------------------|
| **K-Means**  | *0.24 (example)* | *0.50 (example)*      |
| Hierarchical | *0.20 (example)* | *0.60 (example)*      |
| DBSCAN       | *-0.03 (example)*| *862.62 (example)*    |

🔍 **Best Model:** K-Means (based on highest silhouette and lowest DB index)

---

## 🧰 Tech Stack

- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`

## 👨‍💻 Author

Hussain Kachwala
📧 Email Me: hussainkachwala1304@gmail.com
🔗 LinkedIn: www.linkedin.com/in/hussain-kachwala-086990274
