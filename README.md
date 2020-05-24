# Data-Scientist-Capstone-Project
This is the repository for project Data Scientist Capstone Project, a part of the Data Scientist Nanodegree Program by Udacity.

## Project Structure
------
1. [Project Overview](#ProjectOverview)
2. [Project Statement](#ProjectStatement)
3. [Metrics](#Metrics)
4. [Installation](#Installation)
5. [Files](#Files)
6. [Results and Report](#Results&Report)
7. [References](#References)

------
## 1. Project Overview <a name="ProjectOverview"></a> 
Churn Prediction is a popular problem facing in many types of businesses. It minimizes customer defection by predicting which customers are likely to cancel a subscription to a service. 
Though churn prediction was originally used within the telecommunications industry, it has become common practices across many businesses such as banks, insurance firm, and other verticals.

In this project, I'm about to build an end-to-end machine learning model to predict churn customer based on a sample dataset of Sparkify users data and the Apache Spark Machine Learning framework. 
The model is capable of predict which users is likely to churn the music application service.

## 2. Project Statement <a name="ProjectStatement"></a> 
The goal of this project is to create an end-to-end prediction model of churn users of the Sparkify music application; the tasks involved are the following:
1. Preprocessing (load, clean, and transform) the raw dataset in json format with PySpark
2. Analyze the data to define the set of features which can be used to train a predictive model
3. Train classifiers that can determine of a user is churned or not by using Apache Spark Machine Learning framework
4. Select the best and improve the model to get higher results
5. Present the results in a report in Medium blog post([this post](https://medium.com/@think.ai/building-churn-prediction-model-with-apache-spark-machine-learning-b783387811b1)) of the end-to-end process to build an ML model in Apache Spark Machine Learning.

## 3. Metrics
1. **F-1 score** (also F-score or F-measure) is a measure of a test's accuracy. It considers both the precision p and recall r of the test to compute the score. This traditional F-measure or balanced F-score is the harmonic mean of precision and recall. F-1 = 2 x (precision x recall) / (precision + recall)

2. **Accuracy** is a common metric for binary classifiers; it takes into account both true positives and true negatives with equal weight: accuracy = (true_positive + true_negatives)/dataset_size.

## 4. Installation <a name="Installation"></a>
The project is run in Apache Spark environment. Refer to [Apache Spark](https://spark.apache.org) to set up an environment for Spark.
+ PySpark
+ Spark MLlib
+ seaborn
  
## 5. Files <a name="Files"></a>
<pre>
- datasources
- images
- repository
|- Sparkify.ipynb
|- Sparkify.html
- README.md
</pre>

## 6. Results and Report <a name="Results&Report"></a>
The final churn prediction model gets the F-1 score of 78% and Accuracy of 80%.
The report of the this project is presented in this blog post [Building Churn Prediction Model with Apache Spark Machine Learning](https://medium.com/@think.ai/building-churn-prediction-model-with-apache-spark-machine-learning-b783387811b1).

## 7. References <a name="References"></a>
1. [Apache Spark](https://spark.apache.org/docs/latest/api/python/pyspark.sql.html)
2. The Data Scientist Guide to Apache Spark, databricks
