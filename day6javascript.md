# Starting with JavaScript

JavaScript is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions.

## Variables

JS uses variables for storing data values. Variables can ben decalred one of 4 ways:

- Using `var`
- Using `let`
  - If you think the value of the variable can change, use let.
- Using `const`
  - If you want a general rule: always declare variables with const.
- Using nothing

Extra info:

- Always declare JavaScript variables with `var`, `let`, or `const`.
- The `var` keyword is used in all JavaScript code from 1995 to 2015.
- The `let` and `const` keywords were added to JavaScript in 2015.
- If you want your code to run in older browser, you must use `var`.

## Identifiers

- JS variables use unique names called **indentifiers**.
- General rules for creating identifiers:
  - Names can contain letters, digits, underscores, and dollar signs.
  - Names must begin with a letter
  - Names can also begin with `$` and `_`
    - JS treats a dollar sign as a letter, identifiers containing $ are valid variable name. Its use is uncommon unless used as an alias for the main function of a JS library.
    - JavaScript treats underscore as a letter, identifiers containing _ are valid variable names. Using the underscore is not very common in JavaScript, but a convention among professional programmers is to use it as an alias for "private (hidden)" variables.
  - Names are case sensitive (y and Y are different variables)
  - Reserved words (like JavaScript keywords) cannot be used as names

## The =, ==, and === symbols/operators

- In JavaScript, the equal sign (=) is an "assignment" operator, not an "equal to" operator.
- The **equality operator** (==) checks whether its two operands are equal, returning a Boolean result. Unlike the strict equality operator (===), it attempts to convert and compare operands that are of different types.
- The **strict equality operator** (===) checks whether its two operands are equal, returning a Boolean result. Unlike the equality operator (==), the strict equality operator always considers operands of different types to be different.

## Numbers vs Strings in variables

- Strings are written inside double or single quotes. Numbers are written without quotes.
- If you put a number in quotes, it will be treated as a text string.
