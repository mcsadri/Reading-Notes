# Automation

## Reading

### [Python Regular Expressions Tutorial](https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial)

- Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not.
- `re` - Python library that supports regular expressions

### [shutil](https://pymotw.com/3/shutil/)

## Additional Resources

### Videos

#### [Automation Ideas](https://www.youtube.com/watch?v=qbW6FRbaSl0&t=69s)

#### [Automating Your Browser and Desktop Apps](https://www.youtube.com/watch?v=dZLyfbSQPXI)

### Bookmark & Review

- [Watchdog](https://pythonhosted.org/watchdog/)

---

## Reading Questions

- How can you use regular expressions in Python to search for specific patterns in a string, and what is the primary library to work with them?
  - In Python, regular expressions are supported by the `re` module

- What is the purpose of the shutil library in Python, and provide an example of a common use case for file or directory management with this library?
  - The shutil module includes high-level file operations such as copying and archiving.
  - A common use case for the shutil library is to copy or move files or directories from one location to another.

- Explain one automation idea from the assigned material and describe how it can be implemented using Python’s regular expressions and shutil libraries.
  - regex could be used to matching filenames or file extension, and then shutil can move, copy, etc. according to rules established for spcific regex pattern matches.
  