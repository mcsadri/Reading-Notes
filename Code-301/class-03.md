# Passing Functions as Props

## Read

## [React Docs - lists and keys](https://reactjs.org/docs/lists-and-keys.html)

1. What does .map() return?
    1. The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    1. JSX allows embedding any expression in curly braces.
3. Each list item needs a unique ____.
    1. Key. Keys used within arrays should be unique among their siblings. However, they don’t need to be globally unique.
4. What is the purpose of a key?
    1. Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.

### [The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

1. What is the spread operator?
    1. Spread syntax (...) allows an iterable, such as an array or string, to be expanded in places where zero or more arguments or elements are expected.
    2. The spread syntax expands an iterable object, usually an array, though it can be used on any interable, including a string.
2. List 4 things that the spread operator can do.
    1. The … spread operator is useful for many different routine tasks in JavaScript, including the following:
        1. Copying an array
        2. Concatenating or combining arrays
        3. Using Math functions
        4. Using an array as arguments
        5. Adding an item to a list
        6. Adding to state in React
        7. Combining objects
        8. Converting NodeList to an array
3. Give an example of using the spread operator to combine two arrays.

    [A better way to concatenate arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_array_literals)

    ``` javascript
    let arr1 = [0, 1, 2];
    const arr2 = [3, 4, 5];
    arr1 = [...arr1, ...arr2];
    ```

4. Give an example of using the spread operator to add a new item to an array.

    [Spread in array literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_array_literals)

    ``` javascript
    const parts = ['shoulders', 'knees'];
    const lyrics = ['head', ...parts, 'and', 'toes'];
    ```

5. Give an example of using the spread operator to combine two objects into one.

    [Spread in object literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_object_literals)

    ``` javascript
    const obj1 = { foo: 'bar', x: 42 };
    const obj2 = { foo: 'baz', y: 13 };
    const mergedObj = { ...obj1, ...obj2 };
    ```

## Watch

## [How to Pass Functions Between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)

1. In the video, what is the first step that the developer does to pass functions between components?
    1. Adds the expression `increment={this.increment}` to their Person object to pass the prop to the child component. And then calls the method from child component with `this.props.increment()`.
2. In your own words, what does the increment function do?
    1. accepts an argument name from an event handler
    2. creates a new array called ppl from the people array using map()
    3. loops through the people array to find match for name
    4. if name is found add 1 to the count of object p
    5. return p to ppl
    6. updates the state of people to = ppl
3. How can you pass a method from a parent component into a child component?
    1. Pass it as a prop.
4. How does the child component invoke a method that was passed to it from a parent component?
    1. this.props.methodName()

---

## Further Reading

[React Tutorial through ‘Declaring a Winner’](https://reactjs.org/tutorial/tutorial.html)
[React Docs - Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)
