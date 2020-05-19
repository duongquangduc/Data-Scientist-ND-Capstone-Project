# Data Scientist Nanodegree
## Capstone Project
Duc Duong  
May 19th, 2020

## I. Definition

### Project Overview
This is the capstone project of the Data Scientist Nanodegree Program in Udacity. The goal of the project is to analyze and build a predictive model
of churn users for music application Sparkify. There are many users accessing the application everyday. They could use either free-trial or the premium
subscription plan. They can upgrade, downgrade or cancel their subscription of the service at any time. In this project, we will explore a way to predict
churn users with Apache Spark Machine Learning frameworks.


### Problem Statement
Churn Prediction is a polular problem facing in many businesses. It minimizes customer defection by predicting which customers are likely to cancel
a subcription to a service. Though originally used within the telecommunications industry, it has become common practicess across many businesses such as
banks, insurance firm, and other verticals.


### Metrics
I will use the two main metrics to evaluate the model in this project: F-1 Score and Accuracy.
+ F-1 score (also F-score or F-measure) is a measure of a test's accuracy. It considers both the precision *p* and recall *r* of the test to compute the score.
The traiditional F-measure or balanced F-score is the harmonic mean of precision and recall.
F-1 = 2 x (precision x recall) / (precision + recall)

+ Accuracy is a common metric for binary classifiers; it takes into account both true positives and true negatives with equal weight.
accuracy = (true_positive + true_negatives)/dataset_size


## II. Analysis

### Data Exploration
The dataset has 286,500 records and each record has 18 attributes. Refer to the schema of the original dataset as below.

<pre>
root
 |-- artist: string (nullable = true)
 |-- auth: string (nullable = true)
 |-- firstName: string (nullable = true)
 |-- gender: string (nullable = true)
 |-- itemInSession: long (nullable = true)
 |-- lastName: string (nullable = true)
 |-- length: double (nullable = true)
 |-- level: string (nullable = true)
 |-- location: string (nullable = true)
 |-- method: string (nullable = true)
 |-- page: string (nullable = true)
 |-- registration: long (nullable = true)
 |-- sessionId: long (nullable = true)
 |-- song: string (nullable = true)
 |-- status: long (nullable = true)
 |-- ts: long (nullable = true)
 |-- userAgent: string (nullable = true)
 |-- userId: string (nullable = true)
 |-- datetime_ts: string (nullable = true)
 |-- datetime_ts_registration: string (nullable = true)
</pre>

### Exploratory Visualization
1. Gender distribution between churn users and regular users. Refer to the figure as below.
<pre>
+--------+------+-----+
|is_churn|gender|count|
+--------+------+-----+
|       0|     M|   89|
|       0|     F|   84|
|       0|  null|    1|
|       1|     F|   20|
|       1|     M|   32|
+--------+------+-----+
</pre>
![image-1](https://user-images.githubusercontent.com/28558875/82366012-b80f9b80-9a3b-11ea-9280-30fd6a29a20b.png)

2. A comparison of the level of churned users (free vs. paid)

From the chart, we can see that churned users played less number of songs per sessions compared to normal users.
![image-2](https://user-images.githubusercontent.com/28558875/82366034-c1990380-9a3b-11ea-83fa-5ee7fb077ce9.png)


3. A gender distribution for number of songs played per session for churned and regular users

From the chart, we can see that churned users played less number of songs per sessions compared to normal users.
![image-3](https://user-images.githubusercontent.com/28558875/82366063-ccec2f00-9a3b-11ea-8402-90c35e4e73c6.png)

4. A gender distribution for total operations per session between churned and regular users

From the chart, we can see that churn users performed less compared to normal users. And, femla users are more likely to churn.
![image-4](https://user-images.githubusercontent.com/28558875/82366080-d37aa680-9a3b-11ea-95b6-b39ec2929695.png)


### Algorithms and Techniques
I applied the CRISP-DM process for data mining process which consists of the following steps:
+ Business Understanding
+ Data Understanding
+ Data Preparation
+ Data Modeling
+ Evaluation
+ Deployment


### Benchmark
There is no industrial/research benchmark for this dataset. Otherwise, I used different classifiers and select the best one with highest F-1 score and accuracy.


## III. Methodology

### 1. Data Preprocessing
I applied Data Cleaning, Data Transformation, and Feature Engineering steps for the Data Prepocessing phase.

#### Data Cleaninng
+ Rename columns
+ Convert data types: for example, convert from string to timestamp
+ Drop duplicates of userId

#### Data Transformation
+ Derive new columns: is_downgrade, is_churn

After data transformation step, the schema of the dataset looks like this:
<pre>
root
 |-- artist: string (nullable = true)
 |-- auth: string (nullable = true)
 |-- firstName: string (nullable = true)
 |-- gender: string (nullable = true)
 |-- itemInSession: long (nullable = true)
 |-- lastName: string (nullable = true)
 |-- length: double (nullable = true)
 |-- level: string (nullable = true)
 |-- location: string (nullable = true)
 |-- method: string (nullable = true)
 |-- page: string (nullable = true)
 |-- registration: long (nullable = true)
 |-- sessionId: long (nullable = true)
 |-- song: string (nullable = true)
 |-- status: long (nullable = true)
 |-- ts: long (nullable = true)
 |-- userAgent: string (nullable = true)
 |-- userId: string (nullable = true)
 |-- datetime_ts: string (nullable = true)
 |-- datetime_ts_registration: string (nullable = true)
 </pre>

### 2. Feature Engineering
+ Define 9 features from feature 1 to 9 which could be used for the next phase.

Here is the schema of the features set:
<pre>
root
 |-- total_songs: long (nullable = false)
 |-- total_thumbs_up: long (nullable = false)
 |-- total_thumbs_down: long (nullable = false)
 |-- total_lifetime: double (nullable = true)
 |-- total_listen_time: double (nullable = true)
 |-- total_friends: long (nullable = false)
 |-- gender: integer (nullable = true)
 |-- avg_played_songs: double (nullable = true)
 |-- total_artist_listened: long (nullable = false)
 |-- is_churn: integer (nullable = true)
</pre>


### 3. Data Modeling
The steps in this phase include:
+ Vectorize all the features
+ Standarize all input features
+ Split the dataset into train and validation sets
+ Train the model with different classifiers: Random Forest, SVM and Gradient Boosted Trees

Refer to the jupyter notebook for details.

### 3. Model Evaluation & Fine Tuning
The steps in this phase include:
+ Evaluate the model with each classifier by F-1 score and Accuracy. Select the model with highest result.
+ Fine tune the selected model by using Grid Search
+ Evaluate the final one more time.


## IV. Results
The final model reaches F-1 score of 0.8 and accuracy of 78.09 %.
The result of the this project is presented in this post [Building Churn Prediction Model with Apache Spark Machine Learning]().

## V. Conclusion
In this project, I have successfully applied Apache Spark Machine Learning framework to build a Churn Prediction Model.
The model reaches a result of 0.8 for F-1 score and 0.78 for accuracy on 128 MB dataset suggests it could be improved if training on a larger dataset.
The other classifiers or a Neural Network classification based could be experimented to get higher result.


