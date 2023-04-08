# Ten Thousand 2

## Readings

[Python Scope](https://realpython.com/python-scope-legb-rule/)

- The Python scope concept is generally presented using a rule known as the `LEGB rule`:
  - Local: The names that you define in this scope are only available or visible to the code within the scope.
  - Enclosing
  - Global: The names that you define in this scope are available to all your code.
  - Built-in
- The scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on.
  - A name will only be visible to and accessible by the code in its scope.

- Names and Scopes in Python:
  - Since Python is a dynamically-typed language, variables in Python come into existence when you first assign them a value.
  - On the other hand, functions and classes are available after you define them using def or class, respectively.
  - Finally, modules exist after you import them.

- Python Scope vs Namespace
  - Python scopes are implemented as dictionaries that map names to objects.
  - These dictionaries are commonly called namespaces.
  - These are the concrete mechanisms that Python uses to store names. They’re stored in a special attribute called .__dict__.

- Using the LEGB Rule for Python Scope:
  - Local (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.
  - Enclosing (or nonlocal) scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.
  - Global (or module) scope is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.
  - Built-in scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.

- Nested Functions: The Enclosing Scope:
  - Enclosing or nonlocal scope is observed when you nest functions inside other functions.
  - It takes the form of the local scope of any enclosing function’s local scopes.
  - Names that you define in the enclosing Python scope are commonly known as nonlocal names.
  - You can’t modify names in the enclosing scope from inside a nested function unless you declare them as nonlocal in the nested function.
  - Nonlocal names can be accessed from inside nested functions, but they can’t be modified or updated from there.

- Modules: The Global Scope:
  - From the moment you start a Python program, you’re in the global Python scope.
  - Internally, Python turns your program’s main script into a module called __main__ to hold the main program’s execution.
  - The namespace of this module is the main global scope of your program.
  - To inspect the names within your main global scope, you can use dir().
    - If you call dir() without arguments, then you’ll get the list of names that live in your current global scope.
    - When you call dir() with no arguments, you get the list of names available in your main global Python scope.
  - There’s only one global Python scope per program execution. This scope remains in existence until the program terminates and all its names are forgotten.
  - You can access or reference the value of any global name from any place in your code.
  - Whenever you assign a value to a name in Python, one of two things can happen:
    - You create a new name
    - You update an existing name
  
- Good programming practice recommends using local names rather than global names. Here are some tips:
  - Write self-contained functions that rely on local names rather than global ones.
  - Try to use unique objects names, no matter what scope you’re in.
  - Avoid global name modifications throughout your programs.
  - Avoid cross-module name modifications.
  - Use global names as constants that don’t change during your program’s execution.

- Modifying the Behavior of a Python Scope:
  - Python provides two keywords that allow you to modify the content of global and nonlocal names. These two keywords are:
    - global
    - nonlocal
  - The global statement:
    - With the global statement, you can define a list of names inside a function that are going to be treated as global names.
    - The statement consists of the global keyword followed by one or more names separated by commas.
    - All the names that you list in a global statement will be mapped to the global or module scope in which you define them.
    - The use of global is considered bad practice in general.
  - The nonlocal statement:
    - Nonlocal names can be accessed from inner functions, but not assigned or updated.
    - If you want to modify them, then you need to use a nonlocal statement.
    - With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.
    - The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas.
    - Unlike global, you can’t use nonlocal outside of a nested or enclosed function. You can’t use a nonlocal statement in either the global scope or in a local scope.

## Video

[Big O notation is simpler than you might think](https://www.youtube.com/watch?v=dNorFNlDbX0)

- any sequence that reaches a constant sequence after applying enough deltas is called a sequence of polynomial growth
  - aka: O(n^?)
- a constant sequence is: O(1)
- if Δa is eventually bigger than Δb then a is eventually bigger than b (aka Stolz–Cesàro Theorem)
- Types of growth rates:
  - Constant O(1)
  - Logarithmic O(log n)
  - Polynomial O(n^4)
  - Exponential O(5^n)
  - Factorial O(n!)

## Additional Resources

[Rolling Dice Examples](https://artofproblemsolving.com/wiki/index.php/Basic_Programming_With_Python#Program_Example_1_3)

## Reading Questions

1. Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.
    1. The difference between local and global scope is that local variables are only accessible within the function or method in which they are defined, whereas global variables can be accessed from any part of the program. Local variables are created when a function is called and are destroyed when the function returns. Global variables, on the other hand, persist throughout the entire program, and changes made to them inside a function will affect their value outside of the function as well.

2. How do the global and nonlocal keywords work in Python, and in what situations might you use them?
    1. The global and nonlocal keywords are used to access variables from outside of the current scope.
    2. The global keyword is used inside a function to indicate that a variable is in the global scope, rather than the local scope. This means that any changes made to the variable inside the function will affect its value outside of the function as well.
    3. The nonlocal keyword is used inside a nested function to indicate that a variable is in an enclosing scope, rather than the local scope or the global scope. This allows the nested function to access and modify the value of the variable from the enclosing scope.

3. In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.
    1. Big O notation is used to analyze and measure the performance of algorithms by providing an upper bound on the worst-case space and time complexity of an algorithm.

4. Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.
    1. doodah
