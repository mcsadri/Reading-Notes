# Ten Thousand 3

## Reading

[List Comprehensions](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

- List comprehension methods are an elegant way to create and manage lists.
- In Python, list comprehensions are a more compact way of creating lists.
- More flexible than for loops, list comprehension is usually faster than other methods.
- Syntax

  ```python
  my_new_list = [ *expression* for *item* in *list* ]
  ```

  - three ingredients are necessary for a python list comprehension to work:
    - First is the expression we’d like to carry out. *expression* inside the square brackets.
    - Second is the object that the expression will work on. *item* inside the square brackets.
    - Finally, we need an iterable list of objects to build our new list from. *list* inside the square brackets.
  - To understand the list comprehension, imagine it like this: you’re going to perform an expression on each item in the list. The expression will determine what item is eventually stored in the output list.
  - it’s possible to add conditional statements in the form of filters
- Create a List with range()

  ```python
  # construct a basic list using range() and list comprehensions syntax
  # [ expression for item in list ]
  digits = [x for x in range(10)]
  print(digits)
  # output
  [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
  ```

  - the first ‘x’ is the expression. It doesn’t do anything because we’re simply recording the number
  - second ‘x’ represents each item in the list created by the range() method.
  - using the range() method to generate a list of numbers
  - Python iterates(or loops) through each item in that range, and saves a copy of the item in a new list called digits
- Create a List Using Loops and List Comprehension in Python

  ```python
  # create a list of squares using list comprehension
  squares = [x**2 for x in range(10)]
  print(squares)
  ```

- Multiplying Parts of a List

  ```python
  # create a list with list comprehensions: multiply every number in a list by three
  multiples_of_three = [ x*3 for x in range(10) ]
  print(multiples_of_three)
  ```

  - Adding a filter to the list comprehension allows for greater flexibility.
  - By using filters, we can select certain items from the list, while excluding others.
  - This is an advanced feature of lists in Python.

  ```python
  # create list of even numbers 1-20 by filtering where x % 2 == 0
  even_numbers = [ x for x in range(1,20) if x % 2 == 0]
  # output
  [2, 4, 6, 8, 10, 12, 14, 16, 18]
  ```

- Show the first letter of each word using Python
  - List comprehensions can make solving issues involving strings much easier using simplified expressions. These methods can save time and precious lines of code.

  ```python
  # a list of the names of popular authors
  authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison", "Emily Dickson","Stephen King"]
  # create an acronym from the first letter of the author's names
  letters = [ name[0] for name in authors ]
  print(letters)
  # output
  ['E', 'L', 'F', 'T', 'E', 'S']
  ```

  ```python
  # use list comprehension to print the letters in a string
  letters = [ letter for letter in "20,000 Leagues Under The Sea"]
  print(letters)
  # output
  ['2', '0', ',', '0', '0', '0', ' ', 'L', 'e', 'a', 'g', 'u', 'e', 's', ' ', 'U', 'n', 'd', 'e', 'r', ' ', 'T', 'h', 'e', ' ', 'S', 'e', 'a']
  ```

- Lower/Upper case converter using Python
  - Using list comprehension to loop through a string in Python, it’s possible to convert strings from lower case to upper case, and vice versa.

  ```python
  lower_case = [ letter.lower() for letter in ['A','B','C'] ]
  upper_case = [ letter.upper() for letter in ['a','b','c'] ]
  print(lower_case, upper_case)
  # output
  ['a', 'b', 'c'] ['A', 'B', 'C']
  ```

- Print numbers only from a given string
  - Another interesting exercise is to extract numbers from a string. For example, we may have a database of names and phone numbers.

  ```python
  # user data entered as name and phone number
  user_data = "Elvis Presley 987-654-3210"
  phone_number = [ x for x in user_data if x.isdigit()]
  print(phone_number)
  # output
  ['9', '8', '7', '6', '5', '4', '3', '2', '1', '0']
  ```

- Parsing a file using list comprehension
  - It’s also possible to read files in Python using list comprehension.
  - Using list comprehension, we can iterate through the lines of text in the file and store their contents in a new list.
  
  ```python
  # open the file in read-only mode
  file = open("dreams.txt", 'r')
  poem = [ line for line in file ]
  for line in poem:
    print(line)
  ```

- Using functions in list comprehensions
  - Not only can we write our own functions with list comprehensions, but we can also add filters to better control the statements.

  ```python
  # list comprehension with functions
  # create a function that returns a number doubled
  def double(x):
    return x*2
  nums = [double(x) for x in range(1,10)]
  print(nums)
  # output
  [2, 4, 6, 8, 10, 12, 14, 16, 18]
  ```

  - Filtering elements from the list can be done using additional arguments. In the following example, only even numbers are selected.

  ```python
  # add a filter so we only double even numbers
  even_nums = [double(x) for x in range(1,10) if x%2 == 0]
  print(even_nums)
  # output
  [4, 8, 12, 16]
  ```

  - Additional arguments can be added to create more complex logic:

  ```python
  nums = [x+y for x in [1,2,3] for y in [10,20,30]]
  print(nums)
  # ouput
  [11, 21, 31, 12, 22, 32, 13, 23, 33]
  ```

- List comprehension can be used to write more elegant Python code.
- Writing compact code is essential for maintaining programs and working with teams.
- Learning to make use of advanced features like list comprehension will save time and improve productivity.

## Audio

[Debugging with PySnooper](https://www.pythonpodcast.com/pysnooper-python-debugging-episode-241/)

## Additional Resources

[Primer on Decorators](https://realpython.com/primer-on-python-decorators/)

## Discussion Questions

- What is the basic syntax of Python list comprehension, and how does it differ from using a for loop to create a list? Provide an example of a list comprehension that squares the elements in a given list of integers.
  - my_new_list = [ *expression* for *item* in *list* ]
  - squares = [x**2 for x in range(10)]

- What is a decorator in Python?
  Decorators provide a simple syntax for calling higher-order functions. By definition, a decorator is a function that takes another function and extends the behavior of the latter function without explicitly modifying it

- Explain the concept of decorators in Python. How do they work, and what are some common use cases for them? Provide an example of a simple decorator function from the reading.
  - In Python, a decorator is a function that modifies the behavior of another function. Decorators provide a way to add functionality to an existing function without changing its source code. Decorators are defined using the "@" symbol and are placed before the function that they modify.
  - Timing functions, debugging, code, slowing down code, registering plugins, is the user logged in.
  
  ```python
  def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper
  def say_whee():
    print("Whee!")
  say_whee = my_decorator(say_whee)
  ```
  