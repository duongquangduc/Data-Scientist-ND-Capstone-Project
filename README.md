# Data-Scientist-Capstone-Project
This is the repository for project Data Scientist Capstone Project, a part of the Data Scientist Nanodegree Program by Udacity.

### Project Structure
------
1. [Project Overview](#ProjectOverview)
2. [Project Statement](#ProjectStatement)
3. [Metrics](#Metrics)
4. [Installation](#Installation)
5. [Project Components](#ProjectComponents)
6. [Results](#Results)
7. [Files](#Files)
8. [References](#References)

## 1. Project Overview <a name="ProjectOverview"></a> 
This is the capstone project of the Data Scientist Nanodegree Program in Udacity. The goal of the project is to analyze and build a predictive model
of churn users for music application Sparkify. There are many users accessing the application everyday. They could use either free-trial or the premium
subscription plan. They can upgrade, downgrade or cancel their subscription of the service at any time. In this project, we will explore a way to predict
churn users with Apache Spark Machine Learning frameworks.

## 2. Project Statement <a name="ProjectStatement"></a> 
Churn Prediction is a polular problem facing in many businesses. It minimizes customer defection by predicting which customers are likely to cancel
a subcription to a service. Though originally used within the telecommunications industry, it has become common practicess across many businesses such as
banks, insurance firm, and other verticals.

##3. Metrics
I will use the two main metrics to evaluate the model in this project: F-1 Score and Accuracy.
+ F-1 score (also F-score or F-measure) is a measure of a test's accuracy. It considers both the precision *p* and recall *r* of the test to compute the score.
The traditional F-measure or balanced F-score is the harmonic mean of precision and recall.
F-1 = 2 x (precision x recall) / (precision + recall)

+ Accuracy is a common metric for binary classifiers; it takes into account both true positives and true negatives with equal weight.
accuracy = (true_positive + true_negatives)/dataset_size

## 4. Installation <a name="Installation"></a>
The project is run in Apache Spark environment.
  
## 5. Project Components <a name="ProjectComponents"></a> 
- Sparkify.ipynb
- README.md

## 6. Results <a name="Results"></a>
he final model reaches F-1 score of 0.8 and accuracy of 78.09 %.
The result of the this project is presented in this post [Building Churn Prediction Model with Apache Spark Machine Learning](https://medium.com/@think.ai/building-churn-prediction-model-with-apache-spark-machine-learning-b783387811b1).

## 7. Files <a name="Files"></a>
<pre>
- datasources
- images
- reports
|- Capstone-Project-Proposal.md
- repository
|- Sparkify.ipynb
|- Sparkify.html
- Capstone-Project-Report.md
- README.md
</pre>

## 8. References <a name="References"></a>
1. [Apache Spark](https://spark.apache.org/docs/latest/api/python/pyspark.sql.html)
2. The Data Scientist Guide to Apache Spark, Databricks
