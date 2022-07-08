# JavaScript Continued

## Why Functions?

REDUCE
REUSE
RECYCLE

## Control Flow

- Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the *control flow*, such as conditionals and loops.

## Functions

A JavaScript function is

- a block of code designed to perform a particular task
- executed when "something" invokes it (calls it)

Function Syntax

- defined with the `function` keyword, followed by a **name**, followed by parentheses `()`
- names can contain letters, digits, underscores, and dollar signs (same rules as variables)
- parentheses may include parameter names separated by commas: **(parameter1, parameter2, ...)**
- code to be executed, by the function, is placed inside curly brackets: `{}`
- **parameters** are listed inside the parentheses () in the function definition.
- function **arguments** are the **values** received by the function when it is invoked.
- inside the function, the arguments (the parameters) behave as local variables.

## Invocation (but not the churchy kind)

The code inside the function will execute when "something" invokes (calls) the function:

- When an event occurs (when a user clicks a button)
- When it is invoked (called) from JavaScript code
- Automatically (self invoked)

## Return

- When JavaScript reaches a return statement, the function will stop executing.
- If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.
- Functions often compute a return value. The return value is "returned" back to the "caller"

## Other Things

- The `()` operator invokes the function
- functions can be used the same way as variables in formulas, etc.
- varaibles declared within a function are local only to the function.
