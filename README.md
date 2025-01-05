# ML-Models
Build and train the model for analyzing the data of movie industry.

1-	Start from Prediction_ML.ipynb:

-	Introduction
-	Loading and exploring the data
-	Exploratory data analysis
-	Merging the two dataset (sales- metaclean)
-	Visualizing columns (The plot for relation between factors and the box office) 
-	Feature Engineering (Using ANOVA and Pearson correlation) 

2-	Open the notebook for Transformer_1.ipynb: 
Here you can find the code for embedding the reviews. We choose expert review because we need the reviews which are before the releasing date, then we extract the reviews of each movies which the date are before movie release date. After that we did PCA and   save the result in new file which we uploaded separately(expert_transformer_1.xlsx) to use in the main notebook that we have. 

Continue on Prediction_ML.ipynb:
-	Splitting the data to train and test
-	One-hot encoding
-	SVD
-	Training our 3 models (Linear Regression, Random Forest and ANN) 
-	Explainability (SHAP, Counterfactuals) 


And also, you can find all the markdowns and comments with our name before each cell. 

As you can see for filling the null values in production_budget we did knn imputer and filling with median but when we compare the results of correlation the median is higher so we comment the imputer code in the Prediction_ML.ipynb. 
