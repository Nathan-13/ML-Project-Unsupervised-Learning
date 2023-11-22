# Machine Learning Project-Unsupervised Learning

## Project Objectives
The project aims to apply unsupervised learning techniques to "Wholesale Data" to uncover hidden patterns. The process involves exploratory data analysis, pre-processing, KMeans clustering, hierarchical clustering, and Principal Component Analysis (PCA). The goal is to gain insights into the data's structure and identify distinct groups that could inform business strategy and decision-making.

## Project Process

The data set for this project is the "Wholesale Data" dataset containing information about various products sold by a grocery store. The project will be divided into four main parts:

- **Exploratory Data Analysis and Pre-processing:** This involves importing and understanding the dataset, cleaning the data, analyzing and visualizing the relationships between the different variables, detecting and handling outliers, and preparing the data for modelling.

- **KMeans Clustering:** This part involves implementing the KMeans clustering algorithm to group similar data points together. The goal is to identify distinct groups within the data representing different customer types or purchasing behaviours.

- **Hierarchical Clustering:** This part involves implementing hierarchical clustering, another method of grouping similar data points. Unlike KMeans, hierarchical clustering does not require specifying the number of clusters beforehand, and it can provide a more nuanced view of the data's structure.

- **Principal Component Analysis (PCA):** This part involves reducing the dimensionality of the data using PCA. The goal is to transform the data into a lower-dimensional space that retains as much of the original variance as possible. This can make the data more accessible to work with and can help visualize the clusters. See the Unsupervised Learning - Project.ipynb in the notebook folder.

## Project Results
### Exploratory Data Analysis and Pre-processing
- During the EDA step, there were no null values and duplicate rows in the dataset. Each feature's means and standard deviations differ significantly, suggesting that the data covers a wide range of values. This could affect specific machine learning models sensitive to the scale of input features, and feature scaling might be necessary. Also, some features exhibit right skewness (mean > median), which could affect the performance of some machine learning algorithms. However, I observed possible irregularities in the data entry process or the possibility that patient records were not measured and were instead recorded as 0 rather than NULL. Rather than discarding these records with zero values, median values of the respective features were imputed, given the relatively small size of the dataset.

- Also, there were outliers, which could skew the model. Given the small size of the dataset, the capping method was employed to handle outliers for simplicity rather than removing these values.

### Machine Learning Model
- The analysis of the Wholesale dataset using KMeans and Hierarchical clustering models revealed three distinct customer clusters. The first two principal components, which captured significant variance in the data, indicated that features such as Milk, Grocery, and Detergents_Paper play a crucial role in distinguishing customer groups. Outliers representing unique customer behaviours were also identified.

- Comparative evaluation of the models using Silhouette Scores and Davies-Bouldin Indices suggested that the KMeans model performed slightly better in defining clusters and partitioning the data. However, the choice of model should also consider factors like the specific use case, computational efficiency, and interpretability. These insights can guide marketing strategy, customer segmentation, and product development decision-making.

- Principal Component Analysis (PCA) reveals that a few initial components effectively capture a significant portion of the dataset's variance. The correlation between features and principal parts, such as strong positive correlations with Milk, Grocery, and Detergents_Paper in PC1, indicates the importance of specific features in each component. Leveraging these principal components enables customer segmentation based on purchasing behaviours, with high values in PC1 representing customers inclined towards buying Milk, Grocery, and Detergents_Paper products. The interpretability of feature correlations, including their direction (positive or negative), provides valuable insights into customer consumption patterns associated with each principal component.

## Conclusion
From the machine learning models developed and the exploratory data analysis (EDA) conducted, we can conclude that:

- Overall, the K-Means model has performed slightly better than the Hierarchical model on the Wholesale dataset regarding cluster definition and partitioning.
- From a business perspective, this model can guide decision-making in marketing strategy, customer segmentation or consumption patterns, and product development.

## Challenges
Some of the challenges encountered during the project include selecting the right data features and preventing model overfitting, interpreting Principal Components, and the time needed to explore other machine learning tools to understand the models better.

## Future Considerations
- Explore different feature selection approaches, including top correlated features and utilize all available features to assess their impact on model performance.