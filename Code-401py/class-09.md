# Ten Thousand 4

## Reading

### [Dunder Methods](https://dbader.org/blog/python-dunder-methods)

- “dunders” or “special methods” in Python are also sometimes called “magic methods.
- Dunder methods let you emulate the behavior of built-in types.

- To construct `x`\ objects from the `X` class I need a constructor which in Python is the `__init__` dunder
- The constructor takes care of setting up the object

- Object Representation: `__str__`, `__repr__`
  - It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:
    - `__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of `__repr__` is to be unambiguous.
    - `__str__`: The “informal” or nicely printable string representation of an object. *This is for the enduser*.
  - If you wanted to implement just one of these to-string methods on a Python class, make sure it’s `__repr__`.

- Iteration: `__len__`, `__getitem__`, `__reversed__`
  - To iterate over items in reversed order you can implement the `__reversed__` special method

- Operator Overloading for Comparing Accounts: `__eq__`, `__lt__`
  - Why does > work equally well on integers, strings and other objects (as long as they are the same type)? This polymorphic behavior is possible because these objects implement one or more comparison dunder methods.

- Operator Overloading for Merging Accounts: `__add__`
  - In Python, everything is an object. We are completely fine adding two integers or two strings with the + (plus) operator, it behaves in expected ways
  - In general, if you would add your object to a builtin (int, str, …) the `__add__` method of the builtin wouldn’t know anything about your object. In that case you need to implement the reverse add method (`__radd__`) as well.

- Callable Python Objects: `__call__`
  - You can make an object callable like a regular function by adding the `__call__` dunder method.
  - In general, the downside of having a `__call__` method on your objects is that it can be hard to see what the purpose of calling the object is.
  - Most of the time it’s therefore better to add an explicit method to the class.

- Context Manager Support and the With Statement: `__enter__`, `__exit__`
  - A context manager is a simple “protocol” (or interface) that your object needs to follow so it can be used with the with statement. Basically all you need to do is add `__enter__` and `__exit__` methods to an object if you want it to function as a context manager.

- A strategic use of dunder methods make your classes more Pythonic, because they emulate builtin types with Python-like behaviors.

### [Statistics - Probability](https://www.dataquest.io/blog/basic-statistics-in-python-probability/)

- Introduction
  - Probability is a measure of the likelihood of an event occurring.
  - Probability is important in many fields, including statistics, machine learning, and data science.

- Probability Basics
  - Probability is expressed as a number between 0 and 1, with 0 indicating an impossible event and 1 indicating a certain event.
  - The addition rule of probability states that the probability of either of two events occurring is the sum of their individual probabilities. This can be extended to more than two events by using the inclusion-exclusion principle.
  - The multiplication rule of probability states that the probability of two independent events occurring together is the product of their individual probabilities. This can be extended to dependent events by using conditional probability.

- Probability Distributions
  - A probability distribution is a function that describes the likelihood of obtaining the possible values of a random variable.
  - The normal distribution is a commonly used probability distribution that describes many natural phenomena. It is characterized by its mean and standard deviation, and many statistical tests assume that the data is normally distributed.
  - The binomial distribution is a discrete probability distribution that describes the number of successes in a fixed number of independent trials. It can be approximated by the normal distribution when the number of trials is large.

- Hypothesis Testing
  - Hypothesis testing is a statistical method for testing a hypothesis about a population parameter based on a sample of data.
  - The null hypothesis is a statement that assumes there is no difference between the sample and the population.
  - The alternative hypothesis is a statement that assumes there is a difference between the sample and the population.
  - Hypothesis testing involves choosing an appropriate statistical test, calculating a test statistic, and comparing the test statistic to a critical value or p-value to determine if the null hypothesis should be rejected.
  -The p-value is the probability of obtaining a sample as extreme as the observed sample, assuming the null hypothesis is true.
  - The significance level is the probability of rejecting the null hypothesis when it is actually true, and it is typically set to 0.05 or 0.01.
  - Type I error occurs when the null hypothesis is rejected when it is actually true, while Type II error occurs when the null hypothesis is not rejected when it is actually false.
  - The Z-score is a standardized score that measures the number of standard deviations a data point is from the mean of a distribution.

- Three Sigma Rule
  - The Three Sigma Rule states that in a normal distribution, about 68% of the data falls within one standard deviation of the mean, about 95% of the data falls within two standard deviations of the mean, and about 99.7% of the data falls within three standard deviations of the mean.
  - The Three Sigma Rule is useful for identifying outliers in a dataset.

- Conclusion
  - Probability and statistics are fundamental concepts in data science, and Python provides many libraries and tools for working with probability distributions and performing hypothesis testing.
  - Understanding probability and probability distributions is essential for analyzing data and making informed decisions based on data.
  - To become proficient in using probability and statistics in Python, it is important to practice applying these concepts to real-world data problems.

## Video

### [Intro to Statistics](https://www.youtube.com/watch?v=MdHtK7CWpCQ)

### [AI Guru makes $238,800 with misleading paid course. doesn’t credit developers](https://www.youtube.com/watch?v=7jmBE4yPrOs)

## Additional Reference

- [Statistics Module](https://docs.python.org/3/library/statistics.html)

---

## Reading Questions

- What is the purpose of dunder methods in Python? Provide an example of a commonly used dunder method.

- In the video “AI Guru makes $238,800 with misleading paid course,” what was the main ethical issue raised concerning the use of developers’ work, and how might this have been avoided?

- Describe the Python statistics module and give an example of a function within the module that can be used to perform a common statistical operation.
