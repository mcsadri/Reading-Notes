# Debugging

## What Went Wrong - Troubleshooting JavaScript

[What went wrong? Troubleshooting JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_went_wrong)

### Generally speaking, there are two types of errors

- Syntax: an error in the syntax of a coding or programming language, entered by a programmer.
- Logic: an error where the syntax is actually correct but the code produces results different than intended, meaning that program runs successfully but gives incorrect results.

### Fixing Syntax Errors

- Javascript syntax errors are usually accomponied with the following in the browser console:
  - red "x"
  - an error message
  - a "Learn More" link
  - the name of the JavaScript file and the line (and character) where the error was encountered

  [TypeError: "x" is not a function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Not_a_function)

  - It attempted to call a value from a function, but the value is not actually a function. Some code expects you to provide a function, but that didn't happen.
    - A type in the function name
    - Function called on the wrong object
    - Function shares a name with a pre-existing property
    - Using brackets for multiplication
    - Import the exported module correctly

  Note: `console.log()` is a really useful debugging function that prints a value to the console.

  [TypeError: "x" is (not) "y"](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Unexpected_type)

  - The JavaScript exception "x is (not) y" occurs when there was an unexpected type. Oftentimes, unexpected undefined or null values. Also, certain methods, such as Object.create() or Symbol.keyFor(), require a specific type, that must be provided.
    - Invalid cases

### Fixing Logic Errors

### Other Commons Errors

- **SyntaxError: missing ; before statement**: generally means that you have missed a semicolon at the end of one of your lines of code. [SyntaxError: missing ; before statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Missing_semicolon_before_statement)
- **SyntaxError: missing ) after argument list**: generally means that you've missed the closing parenthesis at the end of a function/method call. [SyntaxError: missing ) after argument list](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Missing_parenthesis_after_argument_list)
- **SyntaxError: missing : after property id**: usually relates to an incorrectly formed JavaScript object.
- **SyntaxError: missing } after function body**: generally means that you've missed one of your curly braces from a function or conditional structure.
- **SyntaxError: expected expression, got 'string'** or **SyntaxError: unterminated string literal**: generally means that you've left off a string value's opening or closing quote mark.
  - [SyntaxError: Unexpected token](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Unexpected_token)
  - [SyntaxError: unterminated string literal](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Unterminated_string_literal)

[JavaScript error reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

---

1. Name some key differences between a Syntax Error and a Logic Error. **a syntax error is an erro in the code that prevents its from compiling or executing. A logic error is when compiled/running code produces a result different than intended.**
2. List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them. **Lots of logic errors - fixed with copious use of console.log().**
3. How will this topic continue to influence your long term goals? **Almost everything in this reading topic was review or troubleshooting and debugging I'm already doing. But there are now additional resources I can utilize when encountering a new error message.**

---

## The JavaScript Debugger

[The JavaScript Debugger](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_are_browser_developer_tools#the_javascript_debugger)

> - The JavaScript debugger allows you to watch the value of variables and set breakpoints, places in your code that you want to pause execution and identify the problems that prevent your code from executing properly.
> - Chrome: Open the Developer tools and then select the Sources tab.

### Exploring the Debugger

The Firebox browser has three panes its the JavaScript Debugger

- File List: The first pane on the left contains the list of files associated with the page you are debugging.
- Source Code: Used to set breakpoints where you want to pause execution.
- Watch Expressions and Breakpoints: The right-hand pane shows a list of the watch expressions you have added and breakpoints you have set.

The final two sections only appear when the code is running:

- The **Call stack** section shows you what code was executed to get to the current line.
- **Scopes**, shows what values are visible from various points within your code.

[Google Chrome - Debug JavaScript](https://developer.chrome.com/docs/devtools/javascript/)

---

1. How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development? **The JavaScript debugger is a tool kit that allows the developer to run and pause the execution of their code to identify where bugs occur.**
2. Define what a breakpoint is. **A breakpoints is a location/line of code that has been marked in the debugger to pause execution**
3. What is the call stack? **Shows you what code was executed to get to the current line**

---

## For Further Review

- [Debugging HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML)
- [Debugging CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Debugging_CSS)
