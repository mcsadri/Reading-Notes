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

- Elements are the smallest building blocks of React apps. An element describes what you want to see on the screen.
- Unlike browser DOM elements, React elements are plain objects.
- Rendering an Element into the DOM
  - To render a React element, first pass the DOM element to `ReactDOM.createRoot()`, then pass the React element to `root.render()`.
- Updating the Rendered Element
  - React elements are immutable. You can’t change its children or attributes.
- React Only Updates What’s Necessary
  - React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

### [React - Components & Props](https://reactjs.org/docs/components-and-props.html)

- Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.
- Conceptually, components are like JavaScript functions.
- Function and Class Components
  - The simplest way to define a component is to write a JavaScript function
- Rendering a Component
  - When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.
- Composing Components
  - Components can refer to other components in their output
- Extracting Components
  - A good rule of thumb is that if a part of your UI is used several times (`Button`, `Panel`, `Avatar`), or is complex enough on its own (`App`, `FeedStory`, `Comment`), it is a good candidate to be extracted to a separate component.
- Props are Read-Only
  - Whether you declare a component as a function or a class, it must never modify its own props
  - All React components must act like pure functions with respect to their props.

### [React - State & Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

- State is similar to props, but it is private and fully controlled by the component.
- Converting a Function to a Class

  > - Create an ES6 class, with the same name, that extends React.Component.
  > - Add a single empty method to it called render().
  > - Move the body of the function into the render() method.
  > - Replace props with this.props in the render() body.
  > - Delete the remaining empty function declaration.

- Adding Local State to a Class
  - Class components should always call the base constructor with `props`.
- Adding Lifecycle Methods to a Class
  - In applications with many components, it’s very important to free up resources taken by the components when they are destroyed.
  - We can declare special methods on the component class to run some code when a component mounts and unmounts
  - These methods are called “lifecycle methods”.
- Using State Correctly
  - There are three things you should know about `setState()`:
    - Do Not Modify State Directly
    - State Updates May Be Asynchronous
    - State Updates are Merged
- The Data Flows Down
  - Neither parent nor child components can know if a certain component is stateful or stateless, and they shouldn’t care whether it is defined as a function or a class.
  - This is why state is often called local or encapsulated. It is not accessible to any component other than the one that owns and sets it.
  - A component may choose to pass its state down as props to its child components
  - This is commonly called a “top-down” or “unidirectional” data flow. Any state is always owned by some specific component, and any data or UI derived from that state can only affect components “below” them.

### [React - Handling Events](https://reactjs.org/docs/handling-events.html)

- Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:
  - React events are named using camelCase, rather than lowercase.
  - With JSX you pass a function as the event handler, rather than a string.
  - Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly.
- When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class.
- In JavaScript, class methods are not bound by default. If you forget to bind this.handleClick and pass it to onClick, this will be undefined when the function is actually called.
- Passing Arguments to Event Handlers
  - Inside a loop, it is common to want to pass an extra parameter to an event handler.


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
