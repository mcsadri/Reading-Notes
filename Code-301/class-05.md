# Putting it all together

## [React Docs - Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

1. What is the single responsibility principle and how does it apply to components?
    1. A component should ideally only do one thing.
    2. If it ends up growing, it should be decomposed into smaller subcomponents.
2. What does it mean to build a ‘static’ version of your application?
    1. Build a model version that uses the data model and renders the UI, but does not include any interaction.
3. Once you have a static application, what do you need to add?
    1. Figure out the absolute minimal representation of the state your application needs and compute everything else you need on-demand.
4. What are the three questions you can ask to determine if something is state?
    1. Is it passed in from a parent via props? If so, it probably isn’t state.
    2. Does it remain unchanged over time? If so, it probably isn’t state.
    3. Can you compute it based on any other state or props in your component? If so, it isn’t state.
5. How can you identify where state needs to live?
    1. Identify every component that renders something based on that state.
    2. Find a common owner component (a single component above all the components that need the state in the hierarchy).
    3. Either the common owner or another component higher up in the hierarchy should own the state.
    4. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

## [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)

1. What is a “higher-order function”?
    1. Functions that operate on other functions, either by taking them as arguments or by returning them, are called *higher-order functions*.
2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
    1. 🙃
3. Explain how either map or reduce operates, with regards to higher-order functions.
    1. [When you use Array.map, you provide a function as its only argument, which it applies to every element contained in the array.](https://www.freecodecamp.org/news/higher-order-functions-in-javascript-d9101f9cf528/)
