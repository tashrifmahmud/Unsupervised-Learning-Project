# machine_learning_project-unsupervised-learning
> Tashrif Mahmud

## Project Objective

## Project Outcomes
- Unsupervised Learning: perform unsupervised learning techniques on a wholesale data dataset. The project involves four main parts: exploratory data analysis and pre-processing, KMeans clustering, hierarchical clustering, and PCA.

### Project Description:
In this project, we will apply unsupervised learning techniques to a real-world data set and use data visualization tools to communicate the insights gained from the analysis.

The data set for this project is the "Wholesale Data" dataset containing information about various products sold by a grocery store.
The project will involve the following tasks:

-	Exploratory data analysis and pre-processing: We will import and clean the data sets, analyze and visualize the relationships between the different variables, handle missing values and outliers, and perform feature engineering as needed.
-	Unsupervised learning: We will use the Wholesale Data dataset to perform k-means clustering, hierarchical clustering, and principal component analysis (PCA) to identify patterns and group similar data points together. We will determine the optimal number of clusters and communicate the insights gained through data visualization.

## Project Process:
Details of it can be found in ["Unsupervised Learning - Project.ipynb"]()

### 1. EDA
* Imported csv file to create dataframe
* Checked for missing or incorrect data and overall shape of the dataframe.
* Generated summary statistics to understand the data distribution for each features.
* Created visualizations such as histograms, box plots, scatter plots, and correlation heatmaps to explore relationships and trends between features.
* As data was positively skewed we used log transformation to normalize it as well as remove the impact from outliers.
* Identified and assessed outliers using IQR and visualization to determine their impact and removed them from our data set as part of cleaning.
* Calculated correlations between variables to identify highly correlated and uncorrelated features using correlation heatmap.

### 2. KMeans Clustering
* We set the OMP_NUM_THREADS environment variable to limit the number of threads that MKL uses to avoid memory leaks in windows.
* We also used standard scaler to scale the data.
* To determine how many clusters k we should use we used elbow method plot to score.
* Plotted the clusters using scatterplot for different pair of features.
* We checked the mean of the features for each clusters and grouped them to plot bar chart to better understand the clusters.
* Since the original data is multi-dimensional (6 features), we can apply PCA to reduce the data to two principal components for easier visualization. We do that in later part of this project.

### 3. Hierarchical Clustering
* We used ward method to create dendogram and plotted the dendogram to determine the optimal number of clusters.
* We cut the dendogram to form the clusters and continue with hiearchical clustering.
* Here we also checked the mean of the features for each clusters and grouped them to plot bar chart to better understand the clusters.

### 4. PCA
* First we ran PCA to find the variance explain by each component.
* We built scree model to further understand the optimal number of principal components.
* We analyzed how much each feature impacts our each principal components by accessing the components loading.

### PCA + KMeans Clustering
* We combined PCA with 2 dimensions with Kmeans Clustering for clear visualization and understanding.
* Using PC1 and PC2 we plotted Kmeans Clusters on scatter plot to identify each clusters.
* We also looked at the absolute loading of each component to understand how features relates to them.

## Result and Conclusion
* The original data's positive skew means most customers or businesses have relatively low annual spending, while a smaller number of customers have very high spending and large proportion of revenue comes from these high spenders. 
* Milk and Grocery have a strong positive correlation of 0.78, meaning as milk sales increase, grocery sales tend to increase as well. Detergents_Paper and Grocery also show a strong positive correlation of 0.79, suggesting that these two categories are likely to be purchased together.
* The wholesale data can be divided into 2 main groups. Group 1 of products commonly purchased together are retail items (grocery, milk, detergents), likely driven by household or retail supply needs.
* Group 2 of products are associated with perishables and specialty products (frozen, fresh, delicatessen), distinguishing another aspect of consumer behavior.

## Challenges
* Dropping the outliers could affect the results in some unwanted way.
* The visualization is difficult to understand as we had 6 dimensions of features, it can be improved in the future.

## Future Goals
* Conduct the whole analysis without dropping outliers, and also try imputing them.
* Do more in depth feature selection to get the best features and run our models with those specific features only.


