# Functional Programming

## Reading

### [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

1. What is functional programming?
    1. Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — [Wikipedia](https://en.wikipedia.org/wiki/Functional_programming)
2. What is a pure function and how do we know if something is a pure function?
    1. The strict definition of purity:
        1. It returns the same result if given the same arguments (it is also referred as deterministic)
        2. It does not cause any observable side effects
3. What are the benefits of a pure function?
    1. Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result.
    2. Easier to test. There's no need to mock anything. Not even if the dog quacks like a duck. Be nice.
4. What is immutability?
    1. Unchanging over time or unable to be changed.
    2. When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
5. What is Referential transparency?
    1. If a function consistently yields the same result for the same input, it is referentially transparent.
    2. pure functions + immutable data = referential transparency

#### Extra

-[Functional Programming Jargon](https://github.com/hemanth/functional-programming-jargon)  
-[Master the JavaScript Interview: What is Functional Programming?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)  
-[Master the JavaScript Interview: What is a Pure Function?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976)  
-[Imperative vs Declarative Programming](https://ui.dev/imperative-vs-declarative-programming)  

## Videos

### [Node JS Tutorial for Beginners #6 - Modules and require()](https://www.youtube.com/watch?v=xHLd36QoS4k)

1. What is a module?
    1. Logical sections of code that contain a certain functionality within the applicaiton.
2. What does the word ‘require’ do?
    1. "In NodeJS, require() is a built-in function to include external modules that exist in separate files. require() statement basically reads a JavaScript file, executes it, and then proceeds to return the export object. require() statement not only allows to add built-in core NodeJS modules but also community-based and local modules." [JavaScript require vs import](https://flexiple.com/javascript/javascript-require-vs-import/)
3. How do we bring another module into the file the we are working in?
    1. for example (from [JavaScript Require vs. Import](https://blog.bitsrc.io/javascript-require-vs-import-47827a361b77)):

        ``` javascript
        // built-in moduels
        const http= require('http');
        // local moduels
        const getBlogName = require('./blogDetails.js'
        ```

4. What do we have to do to make a module available?
    1. Inside the module the part(s) of the module intended to be available externally must be explicitly specified with `module.exports = ___`.
