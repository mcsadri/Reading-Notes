# Pythonisms

## Reading

### [Dunder Methods](https://dbader.org/blog/python-dunder-methods)

### [Iterators](https://dbader.org/blog/python-iterators)

### [Generators](https://dbader.org/blog/python-generators)

## Videos (optional)

### [What are Generators](https://realpython.com/lessons/what-are-python-generators/)

## Bookmark & Review

### [Decorators](https://realpython.com/primer-on-python-decorators/)

---

## Reading Questions

- What are dunder methods in Python, and how do they allow for the customization of built-in behavior in classes? Provide an example of a common dunder method and its purpose.
  - In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.
  - A common dunder method in Python is __str__. Its purpose is to define a string representation of an object when the str() function or print() statement is used on an instance of that class.

- Explain the concept of an iterator in Python. How do you create a custom iterator using the iter() and next() methods, and why are they important for enabling iteration in a class?
  - An iterator in Python is an object that allows sequential access to a collection of elements, enabling iteration over its contents one at a time. It provides a way to traverse through data structures like lists, tuples, or dictionaries efficiently, abstracting the complexity of iteration.

- What is a generator in Python, and how does it differ from a regular function? Illustrate your answer with an example of a generator function using the ‘yield’ keyword.
  - A generator in Python is a special type of function that can be paused and resumed, allowing it to produce a sequence of values lazily. Unlike regular functions that return a single value and terminate, generators use the "yield" keyword to produce values one at a time, conserving memory and providing an efficient way to work with large data sets or infinite sequences.

- Define decorators in Python and explain their primary use case. How can you create and apply a custom decorator to a function or method? Provide a simple example to demonstrate this concept.
  - Decorators in Python are a language feature that allows functions to be modified or extended without changing their source code. They are primarily used to wrap functions with additional behavior, such as logging, authentication, caching, or error handling, promoting code reusability and enhancing the overall maintainability of Python programs.
  