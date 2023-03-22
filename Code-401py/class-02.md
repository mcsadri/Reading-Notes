# Testing and Modules

## Reading

### [In Tests We Trust - TDD with Python](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

- Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code that can be written anytime. But Test-Driven Development is a strategy to think (and write!) tests first.
- Tests can be considered as your alive documentation. Be descriptive about it and to say what is expected and what we are testing.
  - The test file name should follow the same name of module name. For instance, if our module is gender.py, our test name should be test_gender.py.
  - It’s ideal to separate the tests folder from production code (the implementation) and to have something like this:

``` python
mymodule/
 — module.py
 — another_folder/
 — — another_module.py
tests/
 — test_module.py
 — another_folder/
 — — test_another_module.py

```

- Structure: A convention widely used is the AAA: **Arrange**, **Act** and **Assert**:
  - Arrange: you need to organize the data needed to execute that piece of code (input);
  - Act: here you will execute the code being tested (exercise the behaviour);
  - Assert: after executing the code, you will check if the result (output) is the same as you were expecting.
- The testing cycle:
  - Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)
  - Write the feature and make the test pass! (you can dance after that)
  - Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)

- Summary:
  - The greatest advantage about TDD is to craft the software design first
  - Your code will be more reliable: after a change you can run your tests and be in peace

### [If name equals main](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)

What does the if `__name__ == “__main__”:` do?

- Before executing code, Python interpreter reads source file and define few special variables/global variables. 
- If the python interpreter is running that module (the source file) as the main program, it sets the special `__name__` variable to have a value `“__main__”`.
- If this file is being imported from another module, `__name__` will be set to the **module’s name**.
- Module’s name is available as value to `__name__` global variable.
  - A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended.
- You can test whether your script is being run directly or being imported by something else by testing `__name__` variable.
  - If script is getting imported by some other module at that time `__name__` will be module name.

Advantages:

- Every Python module has its `__name__` defined and if this is `‘__main__’`, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.
- If you import this script as a module in another script, the `__name__` is set to the name of the script/module.
- Python files can act as either reusable modules, or as standalone programs.
- if `__name__ == “main”:` is used to execute some code **only** if the file was run directly, and not imported.


### [Recursion](https://www.geeksforgeeks.org/recursion/)

---

## Videos

### [What on Earth is Recursion](https://www.youtube.com/watch?v=Mv9NEXX1VHc)

### [Python Modules and Packages Companion Video](https://realpython.com/courses/python-modules-packages/)

---

## Additional Resources:

-[Google for Education: Python Lists](https://developers.google.com/edu/python/lists)
-[Google for Education: Python Strings](https://developers.google.com/edu/python/strings)
-[Python Modules and Packages](https://realpython.com/python-modules-packages/)
-[Pytest Documentation](https://docs.pytest.org/en/latest/)
-[PyTest Tutorial](https://www.guru99.com/pytest-tutorial.html): Up to section `Running tests in parallel`
