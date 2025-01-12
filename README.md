# Machine Learning Project - Unsupervised Learning
> **Tashrif Mahmud**

## Project Outcomes
- Applied unsupervised learning techniques on a wholesale dataset.  
- Focused on four key areas: exploratory data analysis and pre-processing, KMeans clustering, hierarchical clustering, and PCA.

## Project Description
This project explores unsupervised learning on the "Wholesale Data" dataset, containing information about various products sold by a grocery store. The goal is to identify patterns, group similar data points, and visualize insights using unsupervised techniques.

Key Tasks:
1. **Exploratory Data Analysis (EDA) and Pre-processing**: Import, clean, and analyze data to understand relationships, handle missing values, and perform feature engineering.
2. **Unsupervised Learning**: Use KMeans clustering, hierarchical clustering, and PCA to discover patterns, determine the optimal number of clusters, and visualize findings.

Details can be found in the project notebook: [Unsupervised Learning - Project.ipynb](https://github.com/tashrifmahmud/unsupervised-learning-project/blob/main/Unsupervised%20Learning%20-%20Project.ipynb).

---

## Project Process

### 1. Exploratory Data Analysis (EDA)
- Imported CSV to create the dataframe.
- Checked for missing or incorrect data and overall shape of the dataframe.
- Generated summary statistics for each feature to understand data distribution.
- Created visualizations (histograms, box plots, scatter plots, correlation heatmaps) to explore relationships and trends.
- Used log transformation to normalize positively skewed data and reduce the impact of outliers.
- Identified and assessed outliers using IQR and visualizations, then removed them during cleaning.
- Calculated correlations to identify highly correlated features using a correlation heatmap.

### 2. KMeans Clustering
- Used `StandardScaler` to normalize data for clustering.
- Determined the optimal number of clusters using the elbow method.
- Visualized clusters using scatter plots for different feature pairs.
- Analyzed mean feature values for each cluster and created bar charts to understand cluster characteristics.
- Applied PCA to reduce the data's 6 dimensions to 2 principal components for easier visualization.

### 3. Hierarchical Clustering
- Created a dendrogram using the Ward method to determine the optimal number of clusters.
- Formed clusters by cutting the dendrogram and analyzed their characteristics.
- Visualized and grouped clusters using bar charts to identify patterns.

### 4. PCA (Principal Component Analysis)
- Analyzed the variance explained by each principal component.
- Built a scree plot to determine the optimal number of components.
- Evaluated the contribution of each feature to the principal components using component loadings.

### PCA + KMeans Clustering
- Combined PCA (with 2 dimensions) and KMeans clustering for clear visualization.
- Plotted KMeans clusters using PC1 and PC2 to identify patterns.
- Analyzed absolute loadings of features on principal components to understand their relationships.

---

## Results and Conclusions
- **Spending Patterns**: Most customers or businesses have low annual spending, with a few high spenders contributing disproportionately to revenue.
- **Correlations**: 
  - Milk and Grocery have a strong positive correlation (0.78).
  - Detergents_Paper and Grocery are also strongly correlated (0.79), indicating these products are often purchased together.
- **Cluster Insights**:
  - Group 1: Retail items (grocery, milk, detergents) driven by household or retail supply needs.
  - Group 2: Perishables and specialty products (frozen, fresh, delicatessen), highlighting different consumer behavior.

---

## Challenges
- Dropping outliers may unintentionally impact results.
- Visualizing 6-dimensional data was challenging and could be improved.

---

## Future Goals
1. Conduct analysis without dropping outliers and experiment with imputation techniques.
2. Perform in-depth feature selection to identify key features and rerun models with those features only.
