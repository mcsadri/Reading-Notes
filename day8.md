# Operators & Loops

## JavaScript Operators

### Assignment Operators

- Assignment operators assign a value to its left operand based on the value of its right operand. The simple assignment operator is equal (`=`), which assigns the value of its right operand to its left operand. That is, `x = f()` is an assignment expression that assigns the value of f() to x.
  - Assignment (=)
  - Addition Assignment (+=)
  - Subtraction Assignment (-=)
  - Multiplcation Assignment (*=)
  - Division Assignment (/=)
  - Remainder Assignment (%=)
  - Exponentiation Assignment (**=)
  - Logical Nullish Assignment (??=)
  - and lots more

### Comparison Operators

- Comparison operators compare its operands and returns a logical value based on whether the comparison is true.
  - The operands can be numerical, string, logical, or object values.
  - Strings are compared based on standard lexicographical ordering, using Unicode values.
  - If the two operands are not of the same type JavaScript attempts to convert them to an appropriate type for the comparison
  - The sole exceptions to type conversion within comparisons involve the `===` and `!==` operators, which perform strict equality and inequality comparisons.
- The operators, starring as themselves:
  - Equal (==)
  - Not equal (!=)
  - Strict equal (===)
  - Strict not equal (!==)
  - Alligator mouth (>)
  - Alligator mouth or equal (>=)
  - Shark mouth (<)
  - Shark mouth or equal (<=)

## Loopdeloop

There are many different kinds of loops, but they all essentially do the same thing: they repeat an action some number of times*.

- *this could be zero times depening on the loop and condition used

### The super basic types of loops in JavaScript

- `for`
  - A `for` loop repeats until a specified condition evaluates to false.
  - requires 3 expressions in its declaration:

    ```JavaScript
    for ([initialExpression]; [conditionExpression]; [incrementExpression]){
      statement
    }
    ```

  1. The initializing expression `initialExpression`, if any, is executed
  2. The `conditionExpression` expression is evaluated
  3. The `statement` executes
  4. If present, the update expression `incrementExpression` is executed
  5. Rinse, and repeat until `conditionExpression` passes validation

- `while`
  - A `while` statement executes its statements as long as a specified `condition` evaluates to true.
  - If the ==condition== becomes `false`, `statement` within the loop stops executing and control passes to the `statement` following the loop.
  - The `condition` test occurs before `statement` in the loop is executed.
  - If the condition returns `true`, statement is executed and the condition is tested again.
  - If the condition returns `false`, execution stops, and control is passed to the statement following while.

- `do...while`
  - The `do...while` statement repeats until a specified condition evaluates to false.
  - The *statement* is always executed once before the condition is checked.
  - If `condition` is `tru`e, the statement executes again.
  - At the end of every execution, the `condition` is checked.
  - When the `condition` is `false`, execution stops, and control passes to the statement following `do...while`.
