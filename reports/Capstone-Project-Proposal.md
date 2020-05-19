# Data Scientist Nanodegree
## Capstone Proposal: Building an End-to-end Churn Prediction Model with Apache Spark Machine Learning
Duc Duong
May 2020

## Proposal

### Domain Background
Churn Prediction is a polular problem facing in many businesses. It minimizes customer defection by predicting which customers are likely to cancel
a subcription to a service. Though originally used within the telecommunications industry, it has become common practicess across many businesses such as
banks, insurance firm, and other verticals.

The Prediction process is heavily data driven and often utilizes advanced machine learning techniques. In this project, we will build a prediction 
model to predict churn users with Spark and its machine learning frameworks. 

### Problem Statement
The churn action is defined as the cancellation of a user account. Based on the large dataset Sparkify, we need to build a model to predict which users
are likely to cancel the subscription of the service.


### Datasets and Inputs
Input dataset: Sparkify provided by Udacity. The dataset is 128 MB and stored in json format.
A larger dataset which is 12 GB could be used to build the model in a cloud-based environment.


### Solution Statement
The main steps to building a machine learning to predict churn users are as below.
1. Ingest and Clean Datasets: Load and clean the dataset, checking for invalid or missing data - for example, records without userids or sessionids.
2. Data Exploration: Define churn and label based on the definition of churn and perform exploratory data analysis.
3. Feature Engineering: create a set of features that could be used for the prediction.
4. Modeling:
	- Transform features
	- Split dataset into training set, validation set, and test set.
	- Build a predictive model based on Apache Spark ML frameworks.


### Benchmark Model
In this project, I only compare the results of the created model within different classifiers used.

### Evaluation Metrics
F-1 score (also F-score or F-measure) is a measure of a test's accuracy. It considers both the precision *p* and recall *r* of the test to compute the score.
The traiditional F-measure or balanced F-score is the harmonic mean of precision and recall.
F-1 = 2 x (precision x recall) / (precision + recall)

Accuracy is a common metric for binary classifiers; it takes into account both true positives and true negatives with equal weight.
accuracy = (true_positive + true_negatives)/dataset_size

### Project Design
See Solution Statement

