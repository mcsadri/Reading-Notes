# State and Props

## Reading

### [React Lifecycle](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
    1. render
2. What is the very first thing to happen in the lifecycle of React?
    1. The constructor for a React component is called before it is mounted.
3. Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`.
    1. Constructor
    2. render
    3. React Updates
    4. componentDidMount
    5. componentWillUnmount
4. What does componentDidMount do?
    1. used to load network requests, initialize the DOM, or set up subscriptions. Can also be used to setState() (causing a re-render).

## Video

### [React State vs Props](https://www.youtube.com/watch?v=IYvD9oBCuJI)

1. What types of things can you pass in the props?
    1. Like paramaters to a function
    2. Count numbers
    3. Name strings
2. What is the big difference between props and state?
    1. Props handled outside of a component, but are are passed into it.
    2. State is handled inside a compontent.
3. When do we re-render our application?
    1. When state changes in a component it re-renders that portion of the application.
4. What are some examples of things that we could store in state?
    1. Parts of an application that can change due user interaction or input (e.g. a form)

---

## Further Reading

- [React Docs - State and Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
- [React Docs - handling events](https://reactjs.org/docs/handling-events.html)
- [React Tutorial through ‘Developer Tools’](https://reactjs.org/tutorial/tutorial.html)
- [React Bootstrap Documentation](https://react-bootstrap.github.io/)
- [Boootstrap Cheatsheet](https://getbootstrap.com/docs/5.0/examples/cheatsheet/)
- [Bootstrap Shuffle - a class “sandbox”](https://bootstrapshuffle.com/classes)
- [Netlify](https://www.netlify.com/)
