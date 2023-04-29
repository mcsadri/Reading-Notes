# Linear Regressions

## Reading

### [How to Run Linear Regression in Python](https://www.activestate.com/resources/quick-reads/how-to-run-linear-regressions-in-python-scikit-learn/)

note: Scikit-learn is a Python package that simplifies the implementation of a wide range of Machine Learning (ML) methods for predictive data analysis, including linear regression.

- Linear regression can be thought of as finding the straight line that best fits a set of scattered data points.
  - You can then project that line to predict new data points. Linear regression is a fundamental ML algorithm due to its comparatively simple and core properties.

- Linear Regression Concepts
  - Best Fit – the straight line in a plot that minimizes the deviation between related scattered data points.
  - Coefficient – also known as a parameter, is the factor a variable is multiplied by. In linear regression, a coefficient represents changes in a Response Variable (see below).
  - Coefficient of Determination – the correlation coefficient denoted as 𝑅². Used to describe the precision or degree of fit in a regression.
  - Correlation – the relationship between two variables in terms of quantifiable strength and degree, often referred to as the ‘degree of correlation’.  Values range between -1.0 and 1.0.
  - Dependent Feature – a variable denoted as y in the slope equation y=ax+b. Also known as an Output, or a Response.
  - Estimated Regression Line – the straight line that best fits a set of scattered data points
  - Independent Feature – a variable denoted as x in the slope equation y=ax+b. Also known as an Input, or a predictor.
  - Intercept – the location where the Slope intercepts the Y-axis denoted b in the slope equation y=ax+b.
  - Least Squares – a method of estimating a Best Fit to data, by minimizing the sum of the squares of the differences between observed and estimated values.
  - Mean – an average of a set of numbers, but in linear regression, Mean is modeled by a linear function.
  - Ordinary Least Squares Regression (OLS) – more commonly known as Linear Regression.
  - Residual – vertical distance between a data point and the line of regression (see Residual in Figure 1 below).
  - Regression – estimate of predictive change in a variable in relation to changes in other variables (see Predicted Response in Figure 1 below).
  - Regression Model – the ideal formula for approximating a regression.
  - Response Variables – includes both the Predicted Response (the value predicted by the regression) and the Actual Response, which is the actual value of the data point (see Figure 1 below).
  - Slope – the steepness of a line of regression. Slope and Intercept can be used to define the linear relationship between two variables: y=ax+b.
  - Simple Linear Regression – a linear regression that has a single independent variable.

- Linear Regression Class Definition
  - A scikit-learn linear regression script begins by importing the LinearRegression class
  - Although the class is not visible in the script, it contains default parameters that do the heavy lifting for simple least squares linear regression

## Additional Resources

### [Linear Regression in Python](https://realpython.com/linear-regression-in-python/)

- Linear regression is a type of machine learning algorithm used to predict a numerical output variable based on one or more input variables. It is a simple and effective technique for modeling linear relationships between variables, and it can be used for both simple and complex regression problems.
- In linear regression, we assume that there is a linear relationship between the input variables (also called features or independent variables) and the output variable (also called the dependent variable). This means that we can use a linear equation to model this relationship, where the output variable is a linear combination of the input variables and some unknown parameters.
- For example, consider a simple linear regression problem where we want to predict a person's weight based on their height. We can assume that there is a linear relationship between these variables, and we can use a linear equation to model this relationship:
- weight = a * height + b
- Here, a and b are the unknown parameters that we want to estimate based on the data. The goal of linear regression is to find the values of a and b that best fit the data and can be used to make accurate predictions on new data.
- To find these parameters, we use a training dataset that contains examples of the input variables and the corresponding output variable. We then use an optimization algorithm to minimize the difference between the predicted values and the actual values in the training data. This process is known as training the model, and the resulting model can be used to make predictions on new, unseen data.
- Linear regression can be extended to handle more complex regression problems by using multiple input variables and more complex models, such as polynomial regression. However, the basic idea remains the same: we assume a linear relationship between the input variables and the output variable and use a linear equation to model this relationship.
- In Python, we can use popular libraries like Scikit-learn to implement linear regression models with just a few lines of code. These libraries also provide a range of tools for data preprocessing, model evaluation, and hyperparameter tuning, making it easy to apply linear regression to real-world problems.

## Video

### [Introduction to Simple Linear Regressions](https://www.youtube.com/watch?v=KsVBBJRb9TE)

- Regression analysis explores the relationship between a quantitative response variable and one or more explanatory variables
  - if there's only one explanatory variable it's called simple linear regression
  - if there's more than one explanatory variable we call that multiple regression
- x = explanatory (or independent) variable, y = response (or dependent) variable
- Is there strong evidence of a relationship between the explanatory variable, X, and the response variable, Y?

## Bookmark and Review

- [Train & Test Splits](https://towardsdatascience.com/train-test-split-and-cross-validation-in-python-80b61beca4b6)
- [What is Linear Regression](https://www.statisticssolutions.com/what-is-linear-regression/)

---

## Reading Questions

- Can you explain the basic concept of linear regression and its purpose in the context of machine learning and data analysis?
  - Linear regression is a type of machine learning algorithm used to predict a numerical output variable based on one or more input variables.

- Describe the process of implementing a linear regression model using Python’s Scikit Learn library, including the necessary steps and functions.
  - Import the packages and classes that you need.

    ```python
    import numpy as np
    from sklearn.linear_model import LinearRegression
    ```

  - Provide data to work with, and eventually do appropriate transformations.
  - Create a regression model and fit it with existing data.

    ```python
    model = LinearRegression()
    ```

  - Check the results of model fitting to know whether the model is satisfactory.
  - Apply the model for predictions.

    ```python
    y_pred = model.predict(x)
    ```

- What is the purpose of splitting the dataset into train and test sets, and how does this contribute to the evaluation of a machine learning model’s performance?
  - [Split Your Dataset With scikit-learn's train_test_split()](https://realpython.com/train-test-split-python-data/)
