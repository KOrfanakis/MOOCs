# Predicting the Winning College Basketball Team

<p align="center">
  <img width="450" src="https://images.unsplash.com/photo-1583359312696-cbc5d73e5f8d?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1285&q=80">
</p>

<p align="center"><em>Photo by Sheri Hooley (Unsplash)</em></p>

This notebook is an improved version of my final assignment submission for [IBM](https://www.edx.org/school/ibm)’s online course '[Machine Learning with Python: A Practical Introduction](https://www.edx.org/course/machine-learning-with-python-a-practical-introduct)' on [edX](https://www.edx.org/). Its main aim is to practice some of the classification algorithms that we learned in this course. You can view my initial submission [here](https://eu-gb.dataplatform.cloud.ibm.com/analytics/notebooks/v2/5f1b6d25-ddef-45bb-bef9-f716770cdb96/view?access_token=9479c5ce107d2876a3a2aa1b281d6491aa50f228072a576ac6334b0b80ca36ff).

The main focus is on testing our knowledge of machine learning (building and evaluating models). Therefore, some important parts of the typical machine learning workflow are missing, such as a complete exploratory data analysis and a more elaborate pre-processing stage. I intend to fill these gaps in a future version of this notebook.

## Objective

We are data scientists working for a college basketball team. The team coaches have asked us to look at historical data to see which team metrics (individually or in combination) make a team more likely to make it into the Final Four. Our task is to build machine learning models that predict a team’s position (qualification to S16, E8, and F4) based on a set of features. 

We will load a historical dataset from previous seasons, clean the data, and apply different classification algorithms. We are expected to use the following algorithms to build our models:

- k-Nearest Neighbours,
- Decision Tree,
- Support Vector Machine, and
- Logistic Regression.

The results are reported as the accuracy of each classifier, using the following metrics when applicable:

- Accuracy,
- Jaccard index, and
- F1-score.

## Review Criteria

- Build a kNN model using a value of *k* equals five, find the accuracy on the validation data (**1 mark**),
- Determine the accuracy for the first 15 values of *k* on the validation data. (**1 mark**),
- Determine the minimum value for the parameter `max_depth` that improves results for the Decision Tree algorithm (**1 mark**),
- Train a support vector machine model and determine the accuracy on the validation data for each kernel. Find the kernel (linear, poly, rbf, sigmoid) that provides the best score on the validation data and train an SVM model using it (**2 marks**),
- Train a logistic regression model and determine the accuracy of the validation data (set C=0.01) (**2 marks**), and
- Calculate the accuracy, F1 score, and Jaccard Similarity score for each model from above. Use the hyperparameters that performed best on the validation data (**2 marks**).

## Resources Used

Python Version: 3.7<br>
Jupyter Notebook Version: 5.7.8<br>
Packages: pandas, sklearn, numpy, matplotlib, seaborn<br>

