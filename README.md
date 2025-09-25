# mall-customer-clustering
This project applies unsupervised machine learning techniques to segment mall customers based on their shopping behavior. The goal is to identify meaningful customer groups that can help in targeted marketing and business strategy.
---

## 📂 Dataset  
- **Source:** [Customer Shopping Dataset - Retail Sales Data – Kaggle]([https://www.kaggle.com/datasets/mustafakeser4/customer-shopping-dataset](https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset) 
- Contains customer demographics, purchase details, and shopping mall information.  

---

## Steps Performed  
1. **Data Cleaning**  
   - Removed unnecessary columns (Invoice No, Customer ID).  
   - Converted invoice dates into month & weekday features.  
   - Handled categorical variables using Label Encoding.  

2. **Data Scaling & Visualization**  
   - Standardized numerical features using `StandardScaler`.  
   - Boxplots & correlation heatmap to understand distributions and relationships.  

3. **K-Means Clustering**  
   - Applied clustering with different values of *k*.  
   - **Elbow Method** showed a bend at *k = 4*.  
   - **Silhouette Score** was highest at *k = 3 (0.125)* but still meaningful at *k = 4 (0.112)*.  
   - Final choice: **k = 4 clusters** (balance between Elbow and Silhouette).  

 

4. **Cluster Profiling (Mean Values)**  

| Cluster | Gender | Age | Category | Quantity | Price | Payment Method | Customers |
|---------|--------|-----|----------|----------|-------|----------------|-----------|
| 0       | Mostly Female (0.00) | ~43.5 | Category ~2.7 | ~2.7 items | ~350 | Mix (0.44) | 27,424 |
| 1       | Mixed (0.40) | ~43.4 | Category ~2.6 | ~2.9 items | ~488 | Card-based (2.0) | 13,040 |
| 2       | Mostly Male (1.00) | ~43.3 | Category ~2.6 | ~2.9 items | ~488 | Mix (0.43) | 20,514 |
| 3       | Mixed (0.24) | ~43.4 | Higher Category (~3.8) | ~4.3 items | ~2650 | Mix (0.63) | 8,148 |

**Insights:**
- **Cluster 0:** Female, low spenders, mid-range categories.  
- **Cluster 1:** Mixed gender, medium spenders.  
- **Cluster 2:** Male, medium spenders, similar to Cluster 1 but different payment preference.  
- **Cluster 3:** High spenders, buy more items, luxury categories.  

5. **Bonus Methods**  
   - **DBSCAN** clustering to detect dense groups.  
   - **Hierarchical Clustering** with dendrogram visualization.  

---

## Results  
- Best segmentation found with **4 clusters**.  
- Each cluster shows different customer profiles (low spenders vs. high spenders, male vs. female dominance, etc.).  
- Useful insights for mall managers & retailers to design personalized marketing strategies.  

---

## Deliverables  
- Jupyter Notebook (`customer_clustering.ipynb`)  
- README.md (project details & results)  
- Plots: `elbow.png`, `pca.png`  

---
