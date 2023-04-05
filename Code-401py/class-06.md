# Ten Thousand Game 1

## Read

### [How to use Random Module](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

- The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.
- Things the random module can be used for:
  - pick a random number in a given range
  - pick a random element from a python list
  - pick a random card from a deck
  - flip a coin
  - create random strings while choosing passwords
The Random module contains some very useful functions namely:
  - randint() function
    - The randint() function which is defined in the python random module can be used to create random strings within a range.
    - takes two numbers as its input argument
      - first input argument is the start of the range
      - second input argument is the end of the range
    - After execution, the randint() function returns a random integer within the given range
  - random() function
    - The random() function in the python random module is used to generate random numbers between 0 and 1.
    - When executed, the random() function returns a floating point number between 0 and 1.
      - If you want a larger number, you can multiply it by a larger value.
  - choice() function
    - The choice() function is used to select a random element from a collection object like a list, set, tuple, etc.
    - The function takes a collection object as its input argument and returns a random element.
  - randrange() function
    - The randrange() function in the python random module is used to select a random element from a given range.
    - It takes three numbers namely start, stop, and step as input argument.
    - After execution, it generates a randomly selected element from the range(start, stop, step).
  - shuffle() function
    - The shuffle function shuffles the elements in the list in place.
    - The shuffle() function takes a list as an input argument.
    - After execution, the elements of the list are shuffled in a random order.

### [What is Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/)

What is Risk Analysis in Software Testing and how to perform it?

- The probability of any unwanted incident is defined as Risk.
- Risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test.
- Risk Identification:
  - Business Risks
  - Testing Risks
  - Premature Release Risk
  - Software Risks
- Risk Assessment:
  - Effect
  - Cause
  - Likelihood
- Risk Analysis steps:
  - Searching the risk
  - Analyzing the impact of each individual risk
  - Measures for the risk identified

### [Test Coverage](https://martinfowler.com/bliki/TestCoverage.html)

Test coverage. Aka code coverage.

- Test coverage is a useful tool for finding untested parts of a codebase.
- Test coverage is of little use as a numeric statement of how good your tests are.
- Like most aspects of programming, testing requires thoughtfulness.
- Sufficiency of testing is much more complicated attribute than coverage can answer.
- You are (probably) doing enough testing if the following is true:
  - You rarely get bugs that escape into production, and
  - You are rarely hesitant to change some code for fear it will cause production bugs.
- One sign you are testing too much is if your tests are slowing you down

## Watch

### [Big O Notation](https://www.youtube.com/watch?v=v4cd1O4zkGw)

- 4 important rules to know with the Big O:
  - if you have two different steps in your algorithm, you add up those steps
    - if you have a first step that takes O of A time and a second step that takes O of B you would add up those run times and you get Oof A plus B

    ```pseudo
    function doodah():
      do_step_1()     // O(a)
      do_step_2()     // O(b)
                      // O(a+b)
    ```

  - drop constants
    - You do not describe things as O of 2n or O of 3n because you're just looking for how things scale roughly. Is it a linearrelationship, is it a quadratic relationship, so you always drop constants.
  - if you have different inputs you're usually going to use different variables to represent them
    - we have two arrays and we're walking through them to figure out the number of elements in common between the two arrays
      - incorrect: O(N^2)
      - correct: O(a * b)
        - a = len of array a, b = len of array b
    - drop non-dominant terms
      - `¯\_(ツ)_/¯`

## Bookmark & Review

### [Python Random](https://docs.python.org/3/library/random.html)

## Further Reading

### [What is Dependency Injection](https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/)

---

## Reading Questions

1. How can the random module be utilized in Python to generate random numbers or make selections from a list, and what are some common functions available within the module?

2. In the context of software development, what is risk analysis, and what are the key steps involved in conducting a risk analysis for a software project?

3. What is test coverage and why is it an important (or potentially misleading) metric in software testing?

4. What is Big O notation, and how is it used to describe the performance of an algorithm? Give an example of an everyday task (not software related) that demonstrates O(n) time complexity.
