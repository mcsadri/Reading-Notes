# FileIO & Exceptions

## Reading

[Read & Write Files in Python](https://realpython.com/read-write-files-python/)

- Opening a File
  - Use the built-in `open()` function to create a file object.
  - Provide the file name and the desired mode ("r" for reading, "w" for writing, "a" for appending, "x" for exclusive creation).
- Reading from a File
  - Use the `read()` method to read the entire file as a string.
  - Use the `readline()` method to read one line at a time.
  - Use the `readlines()` method to read all lines into a list.
- Writing to a File
  - Use the `write()` method to write a string to a file.
  - Use the `writelines()` method to write multiple lines at once.
- Closing a File
  - Always close a file with the `close()` method when you are done using it.
- With Statement
  - Use the `with` statement to automatically close a file when you are done with it.
  - The `with` statement is safer and more convenient than manually closing the file.
- Binary Files
  -Open a file in binary mode by adding "b" to the mode string.
  - Use the `read()` and `write()` methods to read and write bytes instead of strings.
- Encoding
  - Use the `encoding` parameter when opening a file to specify the encoding (e.g., "utf-8").
  - Use the `errors` parameter to specify how to handle encoding errors.

[Exceptions in Python](https://realpython.com/python-exceptions/)

- Exceptions are raised when something unexpected happens during the execution of a program, such as a divide-by-zero error or a file-not-found error. They allow programs to handle errors gracefully and provide helpful error messages to users.
- Some of the most common exception types include `TypeError`, `ValueError`, `IndexError`, and `FileNotFoundError`. Each type of exception corresponds to a specific type of error that can occur during program execution.
- The `raise` statement allows developers to signal that an error has occurred and to provide information about the error to users. The article provides examples of common use cases for raising exceptions, such as checking for invalid input or handling unexpected conditions.
- The `try` block contains the code that might raise an exception, while the `except` block handles the exception if it occurs. The article provides examples of how to handle different types of exceptions, including handling multiple types of exceptions in a single `except` block.
- You can have multiple except blocks with different exception types listed in them, each with its own handling code. Additionally, you can use the else block to execute code only if no exceptions are raised, and the finally block to execute code regardless of whether an exception was raised or not.
- The `finally` block allows developers to specify code that should be executed regardless of whether an exception is raised or not. This section explains how to use the `finally` block and provides examples of when it might be useful, such as closing files or database connections.
- You can create custom exceptions by subclassing the built-in `Exception` class. Creating custom exceptions allows developers to provide more specific error messages to users and to handle errors in a more granular way. The article provides examples of how to create custom exceptions and how to handle them in code.

--

## Videos

[Read & Write Files in Python - Companion Video](https://realpython.com/courses/reading-and-writing-files-python/)

- only the first 2 videos were available without a subscription

--

## Further Reading

[Reading and Writing Files in Python Quiz](https://realpython.com/quizzes/read-write-files-python/)
