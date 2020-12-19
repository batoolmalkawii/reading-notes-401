# Data Science

## 1. Bird's Eye View:

* `Model` - a set of patterns learned from data.
* `Algorithm` - a specific ML process used to train a model.
* `Training data` - the dataset from which the algorithm learns the model.
* `Test data` - a new dataset for reliably evaluating model performance.
* `Features` - Variables (columns) in the dataset used to train the model.
* `Target variable` - A specific variable you're trying to predict.
* `Observations` - Data points (rows) in the dataset.

#### Supervised Learning: includes tasks for "labeled" data (i.e. you have a target variable).

  * In practice, it's often used as an advanced form of predictive modeling.
  * Each observation must be labeled with a "correct answer."
  * Only then can you build a predictive model because you must tell the algorithm what's "correct" while training it (hence, "supervising" it).
  * Regression is the task for modeling continuous target variables.
  * Classification is the task for modeling categorical (a.k.a. "class") target variables.
  
#### Unsupervised learning: includes tasks for "unlabeled" data (i.e. you do not have a target variable).

  * In practice, it's often used either as a form of automated data analysis or automated signal extraction.
  * Unlabeled data has no predetermined "correct answer."
  * You'll allow the algorithm to directly learn patterns from the data (without "supervision").
  * Clustering is the most common unsupervised learning task, and it's for finding groups within your data.
  
  
  
## 2. Exploratory Analysis:
  
First, you'll want to answer a set of basic questions about the dataset:

  * How many observations do I have?
  * How many features?
  * What are the data types of my features? Are they numeric? Categorical?
  * Do I have a target variable?
  
 Also, , the following can be done:
 1. Plot Numerical Distributions.
 2. Plot Categorical Distributions.
 3. Plot Segmentations.
 4. Study Correlations.
 
 
 
## 3. Data Cleaning:

  * Remove Unwanted observations.
  * Fix Structural Errors.
  * Filter Unwanted Outliers.
  * Handle Missing Data.
  
  
## 4. Feature Engineering:

This is done by applying the following:
  * Infuse Domain Knowledge.
  * Create Interaction Features.
  * Combine Sparse Classes.
  * Add Dummy Variables.
  * Remove Unused Features.


## 5. Algorithm Selection:

##### Why Linear Regression is Flawed?
Simple linear regression models fit a "straight line" (technically a hyperplane depending on the number of features, but it's the same idea). 
In practice, they rarely perform well. We actually recommend skipping them for most machine learning problems.

Their main advantage is that they are easy to interpret and understand. However, our goal is not to study the data and write a research report. 
Our goal is to build a model that can make accurate predictions.

In this regard, simple linear regression suffers from two major flaws:

  1. It's prone to overfit with many input features.
  2. It cannot easily express non-linear relationships.
  
These flaws can be fixed by the following:
 * Regularization.
 * Using Regularized Regression Algos.
 * Using Decision Tree Algos.
 * Using Tree Ensembles.
 
 
 ## 6. Model Training:
 This is done by the following:
   1. Exploring the data.
   2. Cleaning the data.
   3. Engineering new features.






  

