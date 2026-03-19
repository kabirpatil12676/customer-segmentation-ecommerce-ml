<div align="center">

# SmartCart Clustering System

### Customer Segmentation for E-Commerce Using Unsupervised Machine Learning

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-Data-green?logo=pandas&logoColor=white)
![matplotlib](https://img.shields.io/badge/matplotlib-Viz-red?logo=matplotlib&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

</div>

## Problem Statement

SmartCart, a growing e-commerce platform serving 2,200+ customers, faces a critical challenge: **treating all customers identically** results in generic marketing campaigns, inefficient ad spend, and missed revenue opportunities. Without understanding the distinct segments within its customer base, the platform cannot personalize experiences, optimize promotions, or maximize customer lifetime value.

This project uses **unsupervised machine learning** to automatically discover and profile natural customer segments, enabling data-driven, targeted marketing strategies.

## Dataset

| Property | Detail |
|:---|:---|
| **Records** | 2,240 customers |
| **Features** | 22 attributes |
| **Source** | SmartCart E-Commerce Platform |

### Feature Categories

| Group | Features | Description |
|:---|:---|:---|
| **Demographics** | Year_Birth, Education, Marital_Status, Income, Kidhome, Teenhome | Customer background |
| **Enrollment** | ID, Dt_Customer, Recency | Signup date & activity recency |
| **Spending** | MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds | Category-level spend |
| **Purchase Channels** | NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth | Shopping behavior |
| **Feedback** | Complain, Response | Complaints & campaign response |

## Tech Stack

| Tool | Purpose |
|:---|:---|
| **Python 3.13** | Core language |
| **pandas** | Data loading, manipulation & analysis |
| **NumPy** | Numerical computing |
| **matplotlib** | Static visualizations |
| **seaborn** | Statistical plotting & heatmaps |
| **scikit-learn** | StandardScaler, PCA, KMeans, AgglomerativeClustering, silhouette_score |
| **kneed** | Automatic elbow point detection |

## Project Structure

```
SmartCart Clustering System/
├── SmartCart_Clustering_Project.ipynb   # Main analysis notebook
├── smartcart_customers.csv             # Customer dataset (2,240 records)
└── README.md                           # This file
```

### Notebook Sections

1. **Executive Summary** — Business context & key findings
2. **Dataset Overview** — Feature descriptions & data dictionary
3. **Importing Libraries** — Tool setup
4. **Data Loading & Exploration** — Initial data inspection
5. **Data Preprocessing** — Missing values, feature engineering, column cleanup
6. **Exploratory Data Analysis** — Outlier detection, pairplots, correlation heatmap
7. **Feature Encoding & Scaling** — One-Hot Encoding + StandardScaler
8. **Dimensionality Reduction** — PCA (3 components)
9. **Optimal Cluster Selection** — Elbow Method + Silhouette Score, K=4
10. **Clustering Models** — K-Means vs. Agglomerative Clustering
11. **Cluster Characterization** — Segment profiling & visualization
12. **Business Recommendations** — Named segments with marketing strategies
13. **Conclusion** — Findings, impact & future work

## Key Results

### 4 Customer Segments Discovered

| Segment | Name | Income | Spending | Key Trait |
|:---:|:---|:---:|:---:|:---|
| Cluster 0 | **Budget Browsers** | Low-Moderate | Low-Moderate | Deal-responsive, web shoppers |
| Cluster 1 | **Premium Loyalists** | High | High | Store/catalogue preference, quality-driven |
| Cluster 2 | **New & Cautious** | Low | Low | Youngest, most deal-dependent |
| Cluster 3 | **Engaged Enthusiasts** | Moderate-High | High | Best campaign response, fewest children |

### Key Insights

- **Income x Spending** is the strongest segmentation axis (highest correlation in dataset)
- **Premium customers** (Clusters 1 & 3) prefer store/catalogue channels over web deals
- **Budget-conscious customers** (Clusters 0 & 2) have higher web activity but lower conversion
- **Cluster 3** has the best campaign response rate, making it the most efficient target for marketing spend
- Targeted marketing for each segment can improve campaign ROI by **3-5x**

## How to Run

### Prerequisites
```bash
pip install pandas matplotlib seaborn scikit-learn kneed
```

### Run the Notebook
```bash
# Clone the repository
git clone https://github.com/kabirpatil12676/customer-segmentation-ecommerce-ml.git
cd customer-segmentation-ecommerce-ml

# Launch Jupyter Notebook
jupyter notebook SmartCart_Clustering_Project.ipynb
```

Or open in **VS Code**, **Google Colab**, or any Jupyter-compatible environment.

## Author

**Kabir Patil**  
B.Tech (IT) Student

- [LinkedIn](https://www.linkedin.com/in/kabir-patil-7a2a9b30b/)
- [kabirpatil12676@gmail.com](mailto:kabirpatil12676@gmail.com)
- [GitHub](https://github.com/kabirpatil12676)

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
