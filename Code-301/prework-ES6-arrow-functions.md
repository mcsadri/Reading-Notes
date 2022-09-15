# ES6 Arrow Functions in JavaScript

[ECMA-262 6th Edition, The ECMAScript 2015 Language Specification](https://262.ecma-international.org/6.0/)

## Arrow Functions

### [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

### Basics

> - An arrow function expression is a compact alternative to a traditional function expression, but is limited and can't be used in all situations.
> - There are differences between arrow functions and traditional functions, as well as some limitations:
>   - Arrow functions don't have their own bindings to this, arguments or super, and should not be used as methods.
>   - Arrow functions don't have access to the new.target keyword.
>   - Arrow functions aren't suitable for call, apply and bind methods, which generally rely on establishing a scope.
>   - Arrow functions cannot be used as constructors.
>   - Arrow functions cannot use yield, within its body.

#### [Comparing traditional functions to arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#comparing_traditional_functions_to_arrow_functions)

> - The { braces } and ( parentheses ) and "return" are required in some cases.
>   - e.g. if there are **multiple arguments** or **no arguments**, you'll need to re-introduce parentheses around the arguments.
>   - Likewise, if the body requires **additional lines** of processing, you'll need to re-introduce braces **PLUS the "return"**
>   - for named functions arrow expressions are treated like variables

### [Syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#syntax)

> - One parameter: With simple expression return is not needed:

``` javascript
param => expression
(param) => expression
```

> - Multiple params require parentheses. With simple expression return is not needed:

``` javascript
(param1, paramN) => expression
```

> - Multiline statements require body braces and return:

``` javascript
// The parentheses are optional with one single parameter
(param) => {
  const a = 1;
  return a + param;
}
```

> - Multiple params require parentheses. Multiline statements require body braces and return:

``` javascript
(param1, paramN) => {
  const a = 1;
  return a + param1 + paramN;
}
```

#### [Advanced Syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#advanced_syntax)

> - To return an object literal expression requires parentheses around expression:

``` javascript
(params) => ({ foo: "a" }) // returning the object { foo: "a" }
```

> - [Rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters) are supported, and always require parentheses
> - [Default parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters) are supported, and always require parentheses
> - [Destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) within params is supported, and always requires parentheses

### [Description](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#description)

#### [Arrowfunctions used as methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#arrow_functions_used_as_methods)

> - Arrow function expressions are best suited for non-method functions
> - Arrow functions do not have their own `this`.
> - Because a class's body has a `this` context, arrow functions as class fields close over the class's `this` context and the `this` inside the arrow function's body will correctly point to the instance (or the class itself, for static fields). However, because it is a closure, not the function's own binding, the value of `this` will not change based on the execution context.
> - Arrow function properties are often said to be "auto-bound methods"
> - *Class fields are defined on the instance, not on the prototype, so every instance creation would create a new function reference and allocate a new closure, potentially leading to more memory usage than a normal unbound method.*

#### [call, apply, and bind](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#call_apply_and_bind)

> - The [`call`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call), [`apply`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply), and [`bind`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/bind) methods are **NOT suitable** as arrow functions – as they were designed to allow methods to execute within different scopes – because *arrow functions establish `this` based on the scope the arrow function is defined within*.
> - `call`, `apply`, and `bind` work as expected with traditional functions.
> - Perhaps the greatest benefit of using Arrow functions is with methods like `setTimeout()` and `EventTarget.prototype.addEventListener()` that usually require some kind of closure, call, apply or bind to ensure that the function is executed in the proper scope.

#### [No binding of arguments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#no_binding_of_arguments)

> - Arrow functions do not have their own `arguments` object.
> - *You cannot declare a variable called `arguments` in strict mode*
> - In most cases, using rest parameters is a good alternative to using an `arguments` object.

#### Misc

> - [Use of the new opertor](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#use_of_the_new_operator): Arrowfunctions cannot be used as constructors and will throw an error when used with `new`.
> - [Use of prototype property](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#use_of_prototype_property): Arrow functions do not have a `prototype` property.
> - [Use of the yield keyword](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#use_of_the_yield_keyword): The `yield` keyword may not be used in an arrow function's body (except when permitted within functions further nested within it). As a consequence, arrow functions cannot be used as generators.
> - [Function body](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#function_body):
>   - Arrow functions can have either a *concise body* or the usual *block body*.
>   - In a concise body, only an expression is specified, which becomes the implicit return value. In a block body, you must use an explicit `return` statement.
> - [Returning object literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#returning_object_literals):
>   - Keep in mind that returning object literals using the concise body syntax `(params) => {object:literal}` will not work as expected.
>   - This is because the code inside braces ({}) is parsed as a sequence of statements (i.e. `foo` is treated like a label, not a key in an object literal).
>   - You must wrap the object literal in parentheses:

``` javascript
const func = () => ({ foo: 1 });
```

> - [Line breaks](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#line_breaks):
>   - An arrow function cannot contain a line break between its parameters and its arrow.
>   - However, this can be amended by putting the line break after the arrow or using parentheses/braces as seen below to ensure that the code stays pretty and fluffy. You can also put line breaks between arguments.
> - [Parsing order](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#parsing_order):
>   - Although the arrow in an arrow function is not an operator, arrow functions have special parsing rules that interact differently with operator precedence compared to regular functions.
>   - Because `=>` has a lower precedence than most operators, parentheses are necessary to avoid `callback || ()` being parsed as the arguments list of the arrow function.

``` javascript
callback = callback || (() => {});
```

Fin.
