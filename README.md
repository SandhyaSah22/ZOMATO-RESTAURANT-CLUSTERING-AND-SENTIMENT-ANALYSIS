# ZOMATO-RESTAURANT-CLUSTERING-AND-SENTIMENT-ANALYSIS

## Problem Statement

Zomato is an Indian restaurant aggregator and food delivery start-up founded by Deepinder Goyal and Pankaj Chaddah in 2008. Zomato provides information, menus and user-reviews of restaurants, and also has food delivery options from partner restaurants in select cities.

India is quite famous for its diverse multi cuisine available in a large number of restaurants and hotel resorts, which is reminiscent of unity in diversity. Restaurant business in India is always evolving. More Indians are warming up to the idea of eating restaurant food whether by dining outside or getting food delivered. The growing number of restaurants in every state of India has been a motivation to inspect the data to get some insights, interesting facts and figures about the Indian food industry in each city. So, this project focuses on analysing the Zomato restaurant data for each city in India.

The Project focuses on Customers and Company, you have to analyze the sentiments of the reviews given by the customer in the data and made some useful conclusion in the form of Visualizations. Also, cluster the zomato restaurants into different segments. The data is vizualized as it becomes easy to analyse data at instant. The Analysis also solve some of the business cases that can directly help the customers finding the Best restaurant in their locality and for the company to grow up and work on the fields they are currently lagging in.

This could help in clustering the restaurants into segments. Also the data has valuable information around cuisine and costing which can be used in cost vs. benefit analysis

Data could be used for sentiment analysis. Also the metadata of reviewers can be used for identifying the critics in the industry.

# Attribute Information

## Zomato Restaurant names and Metadata

Use this dataset for clustering part

1.Name : Name of Restaurants

2.Links : URL Links of Restaurants

3.Cost : Per person estimated Cost of dining

4.Collection : Tagging of Restaurants w.r.t. Zomato categories

5.Cuisines : Cuisines served by Restaurants

6.Timings : Restaurant Timings

## Zomato Restaurant reviews

Merge this dataset with Names and Matadata and then use for sentiment analysis part

1.Restaurant : Name of the Restaurant

2.Reviewer : Name of the Reviewer

3.Review : Review Text

4.Rating : Rating Provided by Reviewer

5.MetaData : Reviewer Metadata - No. of Reviews and followers

6.Time: Date and Time of Review

7.Pictures : No. of pictures posted with review

# Steps involved:

## Null values Treatment

The data set had null values out of which we replaced some with the mean of the feature some by zero and dropped some observations which were almost filled with null values.

## Outliers treatment

Isolation Forests(IF), similar to Random Forests, are built based on decision trees. And since there are no predefined labels here, it is an unsupervised model.IsolationForests were built based on the fact that anomalies are the data points that are “few and different”.In an Isolation Forest, randomly sub-sampled data is processed in a tree structure based on randomly selected features. The samples that travel deeper into the tree are less likely to be anomalies as they require more cuts to isolate them. Similarly, the samples which end up in shorter branches indicate anomalies as it was easier for the tree to separate them from other observations.

## Exploratory Data Analysis

We performed univariate and bivariate analyses. This process helped us figure out various aspects and relationships among variables. It gave us a better idea of which feature behaves in which manner.

## Encoding of categorical columns

We used One Hot Encoding(converting to dummy variables) to produce binary integers of 0 and 1 to encode our categorical features because categorical features that are in string format cannot be understood by the machine and needs to be converted to the numerical format.

## Standardization of features

Our main motive through this step was to scale our data into a uniform format that would allow us to utilize the data in a better way while performing fitting and applying different algorithms to it. The basic goal was to enforce a level of consistency or uniformity to certain practices or operations within the selected environment.

## Fitting different models

For modeling, we tried various algorithms like:

* Clustering

* K means clustering

* Hierarchical clustering

* MultinomialNB

* Logistic Regression

* Decision Tree

* Random Forest Classification

* XGBoost Classification

* LightGBM Classification

## Tuning the hyperparameters for better recall

It is necessary to tune the hyperparameters of respective algorithms to improve accuracy and avoid overfitting when using tree-based models such as Random Forest Classifier and XGBoost classifier. The best set of hyperparameters was determined using a grid search algorithm.

## Features Explainability

We have applied SHAP on the XGBoost and CatBoost model to determine the features that were most important while predicting an instance and also build a feature importance graph to find out which features were important and which were redundant in a model

## Deciding number of cluster

Elbow Method 

From the above graph we selected the number of cluster(k) should be between 3 and 5

## Performance Matrix

Clustering

## Silhouette score 

It can be seen that the silhouette score for k=3 is the highest

Sentiment Analysis




## Conclusion

Based on the silhouette score plot and elbow plot, we decided on 3 clusters that were grouped using KMeans clustering and Hierarchical clustering.
Best models we found for sentiment analysis(Supervised) are Lightgbm and logistic regression



