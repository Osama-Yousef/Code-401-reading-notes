# Read:16 Summary
## Data Science Primer
* `Machine learning` : is a comprehensive approach to solving problems...
* Machine learning is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions.For true machine learning, the computer
must be able to learn patterns that it's not explicitly programmed to identify.
* A task is a specific objective for your algorithms.
* Algorithms can be swapped in and out, as long as you pick the right task.
* In fact, you should always try multiple algorithms because you most likely won't know which one will perform best for your dataset.
* The two most common categories of tasks are :
  * Supervised Learning :  includes tasks for "labeled" data (i.e. you have a target variable).
    * In practice, it's often used as an advanced form of predictive modeling.

    * Each observation must be labeled with a "correct answer."

    * Only then can you build a predictive model because you must tell the algorithm what's "correct" while training it (hence, "supervising" it).

    * Regression is the task for modeling continuous target variables.

    * Classification is the task for modeling categorical (a.k.a. "class") target variables.
  * Unsupervised Learning : includes tasks for "unlabeled" data (i.e. you do not have a target variable).
    * In practice, it's often used either as a form of automated data analysis or automated signal extraction.

    * Unlabeled data has no predetermined "correct answer."

    * You'll allow the algorithm to directly learn patterns from the data (without "supervision").

    * Clustering is the most common unsupervised learning task, and it's for finding groups within your data.

  ### The 3 Elements of Great Machine Learning :
    * #1: A skilled chef (human guidance) : you'll need to make dozens of decisions along the way.In fact, the very first major decision is how to 
    road-map your project for guaranteed success.

    * #2: Fresh ingredients (clean, relevant data) : The second essential element is the quality of your data.Professional data scientists spend most their 
    time understanding the data, cleaning it, and engineering new features.




    * #3: Don't overcook it (avoid overfitting) : One of the most dangerous pitfalls in machine learning is overfitting. An overfit model has "memorized" 
    the noise in the training set, instead of learning the true underlying patterns.

  ### There are 5 core steps:
    * Exploratory Analysis : First, "get to know" the data. This step should be quick, efficient, and decisive.
    * Data Cleaning : Then, clean your data to avoid many common pitfalls. Better data beats fancier algorithms.
    * Feature Engineering : Next, help your algorithms "focus" on what's important by creating new features.
    * Algorithm Selection : Choose the best, most appropriate algorithms without wasting your time.
    * Model Training : Finally, train your models. This step is pretty formulaic once you've done the first 4.

  ### there are other situational steps as well:
    * Project Scoping : Sometimes, you'll need to roadmap the project and anticipate data needs.
    * Data Wrangling : You may also need to restructure your dataset into a format that algorithms can handle.
    * Preprocessing : Often, transforming your features first can further improve performance.
    * Ensembling : You can squeeze out even more performance by combining multiple models.
---------------------------------------------------------------------------------------------------------------------------------------------------------
## Exploratory Analysis
* Proper exploratory analysis is about answering questions. It's about extracting enough insights from your dataset to course correct before you get lost in the weeds.
* The purpose of exploratory analysis is to "get to know" the dataset. Doing so upfront will make the rest of the project much smoother, in 3 main ways:
  * You’ll gain valuable hints for Data Cleaning (which can make or break your models).

  *  You’ll think of ideas for Feature Engineering (which can take your models from good to great).

  * You’ll get a "feel" for the dataset, which will help you communicate results and deliver greater impact.
* exploratory analysis for machine learning should be quick, efficient, and decisive... not long and drawn out!
* First, you'll want to answer a set of basic questions about the dataset:
  * How many observations do I have?

  * How many features?

  * What are the data types of my features? Are they numeric? Categorical?

  * Do I have a target variable?

* `correlations` : allow you to look at the relationships between numeric features and other numeric features.Correlation is a value between -1 and 1 that
represents how closely two features move in unison. You don't need to remember the math to calculate them
-------------------------------------------------------------------------------------------------------------------------------------------------------------
## Data Cleaning
* `Data cleaning` : is one those things that everyone does but no one really talks about. Sure, it’s not the "sexiest" part of machine learning. And no, there
aren’t hidden tricks and secrets to uncover.
* However, proper data cleaning can make or break your project. Professional data scientists usually spend a very large portion of their time on this step.

***Better data beats fancier algorithms.***

* Data cleanng steps :
  * Remove Unwanted observations from datasets : This includes duplicate or irrelevant observations.
  * Fix Structural Errors : Structural errors are those that arise during measurement, data transfer, or other types of "poor housekeeping."For instance, you can 
  check for typos or inconsistent capitalization. This is mostly a concern for categorical features, and you can look at your bar plots to check.

  * Filter Unwanted Outliers : Outliers can cause problems with certain types of models. For example, linear regression models are less robust to outliers than decision tree 
  models.In general, if you have a legitimate reason to remove an outlier, it will help your model’s performance.However, outliers are innocent until proven guilty. 
  You should never remove an outlier just because it’s a "big number." That big number could be very informative for your model.

  * Handle Missing Data : Missing data is a deceptively tricky issue in applied machine learning.First, just to be clear, you cannot simply ignore missing values 
  in your dataset. You must handle them in some way for the very practical reason that most algorithms do not accept missing values.
-----------------------------------------------------------------------------------------------------------------------------------------------------
## Feature Engineering
* Feature engineering is about creating new input features from your existing ones.
* feature engineering steps :
  * Infuse Domain Knowledge : You can often engineer informative features by tapping into your (or others’) expertise about the domain.
  * Create Interaction Features : The first of these heuristics is checking to see if you can create any interaction features that make sense. These are combinations of 
  two or more features.By the way, in some contexts, "interaction terms" must be products between two variables. In our context, interaction features 
  can be products, sums, or differences between two features.

  * Combine Sparse Classes : Sparse classes (in categorical features) are those that have very few total observations. They can be problematic for certain machine
  learning algorithms, causing models to be overfit.

  * Add Dummy Variables : Dummy variables are a set of binary (0 or 1) variables that each represent a single class from a categorical feature.

  * Remove Unused Features : Unused features are those that don’t make sense to pass into our machine learning algorithms. Examples include: ID columns/Features that 
  wouldn't be available at the time of prediction/Other text descriptions

 ---------------------------------------------------------------------------------------------------------------------------------------------------------------
 ## Algorithm Selection
* 5 very effective machine learning algorithms for regression tasks. 
  * Linear Regression is Flawed
  * Regularization in Machine Learning : is a technique used to prevent overfitting by artificially penalizing model coefficients.It can discourage large coefficients
  (by dampening them).

  * Regularized Regression Algos : it has many types such as : Lasso Regression / Ridge Regression / Elastic-Net

  * Decision Tree Algos : Decision trees model data as a "tree" of hierarchical branches. They make branches until they reach "leaves" that represent predictions.

  * Tree Ensembles : Ensembles are machine learning methods for combining predictions from multiple separate models. There are a few different methods for
  ensembling
--------------------------------------------------------------------------------------------------------------------------------------------------------------
## Model Training
* It have these steps :
  * Split Dataset

  * Hyperparameters : Hyperparameters express "higher-level" structural settings for algorithms.
  * Cross-Validation :  is a method for getting a reliable estimate of model performance using only your training data.
  * Fit and Tune Models 

  * Select Winning Model : you'll have 1 "best" model for each algorithm that has been tuned through cross-validation. Most importantly, you've only
  used the training data so far.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------




 







 
















