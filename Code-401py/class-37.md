# React 1

## ES6 Overview

### [ES6 Syntax and Feature Overview](https://www.taniarascia.com/es6-syntax-and-feature-overview/)

- ECMAScript 2015, aka ES6
- Variable and Constant declaration

  > | Keyword | Scope | Hoisting | Can Be Reassigned | Can Be Redeclared |
  > |---|---|---|---|---|
  > | var | Function scope | Yes | Yes | Yes |
  > | let | Block scope | No | Yes | No |
  > | const | Block scope | No | No | No |

- Arrow function syntax
  - Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

  > - let func = (a) => {} // parentheses optional with one parameter
  > - let func = (a, b, c) => {} // parentheses required with multiple parameters

  - [MDN Reference: Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
- Template literals
  - Concatenation/string interpolation)
    - Expressions can be embedded in template literal strings.

    > - let str = `Release Date: ${date}`

    - [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals#Expression_interpolation)

- Implicit returns
  - The return keyword is implied and can be omitted if using arrow functions without a block body.
  
  > - let func = (a, b, c) => a + b + c

  - [MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#Function_body)

- Key/property shorthand
  - ES6 introduces a shorter notation for assigning properties to variables of the same name.

    > - let obj = {a, b,}

    - [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#Property_definitions)
- Method definition shorthand
  - The `function` keyword can be omitted when assigning methods on an object.
- Destructuring (object matching)
  - Use curly brackets to assign properties of an object to their own variable.
- Array iteration (looping)
  - A more concise syntax has been introduced for iteration through arrays and other iterable objects.
- Default parameters
  - Functions can be initialized with default parameters, which will be used only if an argument is not invoked through the function.
- Spread syntax
  - Spread syntax can be used to expand an array.
  - Spread syntax can be used for function arguments.
- Classes/constructor functions
  - ES6 introducess the `class` syntax on top of the prototype-based constructor function.
- Inheritance
  - The `extends` keyword creates a subclass.
- Modules - export/import
  - Modules can be created to export and import code between files.
- Promises/callbacks
  - Promises represent the completion of an asynchronous function. They can be used as an alternative to chaining functions.

## React

### [React - Hello World](https://reactjs.org/docs/hello-world.html)

- React is a JavaScript library

### [React - JSX](https://reactjs.org/docs/introducing-jsx.html)

- JSX is a syntax extension to JavaScript
  - Use it with React to describe what the UI should look like
  - JSX produces React “elements”.
  - React separates concerns with loosely coupled units called “components” that contain both markup and logic
  - You can put any valid JavaScript expression inside the curly braces in JSX
  - After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.
  - Specifying Attributes with JSX
    - You may use quotes to specify string literals as attributes
    - You may also use curly braces to embed a JavaScript expression in an attribute
  - JSX Prevents Injection Attacks
    - React DOM escapes any values embedded in JSX before rendering them

### [React - Rendering Elements](https://reactjs.org/docs/rendering-elements.html)

### [React - Components & Props](https://reactjs.org/docs/components-and-props.html)

### [React - State & Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

### [React - Handling Events](https://reactjs.org/docs/handling-events.html)

## Tailwind CSS

### [Utility First CSS](https://tailwindcss.com/docs/utility-first)

### [Tailwind in a few min minutes](https://www.youtube.com/watch?v=pB1oed_10IA)

## Next.js

### [Learn Next.js](https://nextjs.org/learn/basics/create-nextjs-app)

### [Why to use Next.js](https://www.youtube.com/watch?v=rtgbaKBhdkk)

## Reading Questions

- In the context of ES6 Syntax and Feature Overview, what are three key features introduced in ES6 that improve upon the previous version of JavaScript, and briefly explain their benefits?

- After reading “Tailwind in 15 minutes,” can you describe the purpose of utility classes in Tailwind CSS and provide an example of how to use them to style an HTML element?

- Based on “Why to use Next.js,” explain the main advantages of using Next.js for web development, and provide a brief comparison between traditional client-side rendering and Next.js’s server-side rendering approach.
