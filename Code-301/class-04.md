# React and Forms

## [React Docs - Forms](https://reactjs.org/docs/forms.html)

1. What is a ‘Controlled Component’?
    1. A Controlled Component is a React component that renders a form and also controls what happens in that form on subsequent user input.
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why?
    1. Update the state with their responses as soon as they enter them.
    2. The user response/value can be passed to other UI elements, or reset it from other event handlers.
3. How do we target what the user is entering if we have an event handler on an input field?
    1. Add a `name` attribute to the input element.

## [The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

1. Why would we use a ternary operator?
    1. Collapses if/else-if/ do a single line while preserving the ability to nest conditions.
2. Rewrite the following statement using a ternary statement:

    ```javascript
    if(x===y){
    console.log(true);
    } else {
    console.log(false);
    }
    ```

    ```javascript
    x === y ? console.log(true) : console.log(false);
    ```

---

## Further Reading

- [React Bootstrap - Forms](https://react-bootstrap.github.io/forms/overview/)
- [React Docs - conditional rendering](https://reactjs.org/docs/conditional-rendering.html)
