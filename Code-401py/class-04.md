# Classes and Objects, Recursion, & pytest

## Reading

### [Classes and Objects](https://www.learnpython.org/en/Classes_and_Objects)

Classes and Objects

> - Objects are an encapsulation of variables and functions into a single entity.
> - Objects get their variables and functions from classes.
> - Classes are essentially a template to create your objects.

Accessing Object Variables

> - You can create multiple different objects that are of the same class(have the same variables and functions defined).
> - However, each object contains independent copies of the variables defined in the class.

Accessing Object Functions

> - To access a function inside of an object you use notation similar to accessing a variable.

init()

> - The `__init__()` function, is a special function that is called when the class is being initiated. It's used for assigning values in a class.

### [Thinking Recursively](https://realpython.com/python-thinking-recursively/) (Optional:`Naive Recursion` is Naive section and beyond)

> - A recursive function is a function defined in terms of itself via self-referential expressions.
> - A recursive function will continue to call itself and repeat its behavior until some condition is met to return a result.
> - All recursive functions share a common structure made up of two parts: base case and recursive case.

Maintaining State:

> - When dealing with recursive functions, each recursive call has its own execution context, so to maintain state during recursion you have to either:
>   - [Thread](https://realpython.com/intro-to-python-threading/) the state through each recursive call so that the current state is part of the current call’s execution context
>   - Keep the state in global [scope](https://realpython.com/python-namespaces-scope/).

- Allegedly, using global mutable state is evil.

Recursive Data Structures in Python

> - A data structure is recursive if it can be deﬁned in terms of a smaller version of itself.
>   - A [list](https://realpython.com/python-lists-tuples/) is an example of a recursive data structure.
> - Recursive data structures and recursive functions go together like bread and butter.
>   - The recursive function’s structure can often be modeled after the definition of the recursive data structure it takes as an input.

`lru_cache`

> - [lru_cache](https://realpython.com/lru-cache-python/) is a [decorator](https://realpython.com/primer-on-python-decorators/) that caches the results.
> - Thus, we avoid recomputation by explicitly checking for the value before trying to compute it.
> - One thing to keep in mind about `lru_cache` is that since it uses a dictionary to cache results, the positional and keyword arguments (which serve as keys in that dictionary) to the function must be hashable.

Misc.

> - Python doesn’t have support for [tail-call elimination](https://en.wikipedia.org/wiki/Tail_call).
>   - you can cause a stack overflow if you end up using more stack frames than the [default call stack depth](https://docs.python.org/3.6/library/sys.html#sys.getrecursionlimit)
>   - Keep this limitation in mind for programs that require deep recursion.
> - Python’s mutable data structures don’t support structural sharing
>   - treating them like [immutable data structures](https://en.wikipedia.org/wiki/Persistent_data_structure) is going to negatively affect your space and [GC (garbage collection)](https://realpython.com/python-memory-management/#garbage-collection) efficiency because you are going to end up unnecessarily copying a lot of mutable objects.

### [Pytest Fixtures and Coverage](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)




---

## Review Questions

1. What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?

2. Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?

3. What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project.

---

## Further Reading

-[Pytest Fixtures](https://docs.pytest.org/en/latest/fixture.html)
