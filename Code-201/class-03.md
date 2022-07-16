# HTML Lists, Control Flow with JS, and the CSS Box Model

## HTML Lists

### Ordered Lists

The `<ol>` element is used to represent a list of numbered items.

note:
> Flow content is a broad category that encompasses most elements that can go inside the `<body>` element, including heading elements, sectioning elements, phrasing elements, embedding elements, interactive elements, and form-related elements. It also includes text nodes (but not those that only consist of white space characters). ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories#flow_content))

#### The `<ol>` element atrributes

- [global attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes)
- `reversed` reverses the numbering order
- `start` sets the numbering starting point
- `type` set the numbering type

#### Usage Notes

> - ordered list items display with a preceding marker, such as a number or letter.
> - The `<ol>` and `<ul>` elements may nest as deeply as desired, alternating between `<ol`> and `<ul>` however you like.
> - The `<ol>` and `<ul>` elements both represent a list of items. The difference is with the `<ol>` element, the order is meaningful.
> - To determine which list to use, try changing the order of the list items; if the meaning changes, use the `<ol>` element — otherwise you can use `<ul>`.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol#usage_notes))

### Unordered Lists

The `<ul>` element is used to represent a list of unordered/unnumbered items in a bullet list.

#### The `<ul>` element atrributes

- [global attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes)
- `compact` dont use this attribute. use CSS to modify `line-height` instead
- `type` sets the bullet style: cicrle, disc, or square (the WebTV interface also supports triangle)
- if there is no type specification and not CSS `list-style-type` property the the user agent (browser) will auto-select the type based on nesting level.

Usage Notes

> - The `<ul>` element is for grouping a collection of items that do not have a numerical ordering, and their order in the list is meaningless.
> - The `<ul>` and `<ol>` elements may be nested as deeply as desired. Moreover, the nested lists may alternate between `<ol>` and `<ul>` without restriction.
> - The `<ol>` and `<ul>` elements both represent a list of items. They differ in that, with the `<ol>` element, the order is meaningful.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul#usage_notes))

---

1. When should you use an *unordered list* in your HTML document? **when the order of the listed items is irrelevant***
2. How do you change the *bullet style* of unordered list items? **use the type attribute in the `<ul>` element opening tag**
3. When should you use an *ordered list* vs an *unorder list* in your HTML document? **ordered lists should be used when list numbered items in order**
4. Describe two ways you can change the numbers on *list items* provided by an *ordered list*? **The `start` attribute can be used to change the numeric starting point to something different than 1. Or using the `type` attribute can change the numbering to Roman Numerals or letters.**

---

## CSS Box Model

Everything in CSS is surrounded by a box. Learning how to modifying these boxes is the key the making complex layouts with CSS. This is called the **CSS Box Model**.

Generally speaking, there are two kinds of boxes: **block boxes** and **inline boxes**. Boxes have an **inner display type** and an **outer display type**. Various values can be set using the `display` property.

### Outer Display Type

Boxes with an outer display type of `block` will:

> - The box will break onto a new line.
> - The `width` and `height` properties are respected.
> - Padding, margin and border will cause other elements to be pushed away from the box.
> - The box will extend in the inline direction to fill the space available in its container. In most cases, the box will become as wide as its container, filling up 100% of the space available.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#outer_display_type))

Boxes with an `inline` outer display type will:

> - The box will not break onto a new line.
> - The `width` and `height` properties will not apply.
> - Vertical padding, margins, and borders will apply but will not cause other inline boxes to move away from the box.
> - Horizontal padding, margins, and borders will apply and will cause other inline boxes to move away from the box.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#outer_display_type))

### Inner Display Type

> - Boxes also have an inner display type, which dictates how elements inside that box are laid out.
> - Block and inline layout is the default way things behave on the web. By default and without any other instruction, the elements inside a box are also laid out in normal flow and behave as block or inline boxes.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#inner_display_type))

Parts of a box:

- Content box: The area where your content is displayed.
- Padding box: The padding sits between the border and the content area and is used to push the content away from the border.
- Border box: The border is drawn between the margin and the padding of a box.
- Margin box: The margin is an invisible space around your box. It pushes other elements away from the box.

---

1. Describe the CSS properties of *margin* and *padding* as characters in a story. What is their role in a story titled: “The Box Model”? ** In "The Box Model" the *margin* is a content's sci-fi force field that pushes away (with positive or negative force). Whereas the *padding* is the sci-fi Heisenberg Compensator. I don't know what I'm talking about.
2. List and describe the four parts of an HTML elements box as referred to by the *box model*.

- **Content box: The area where your content is displayed.**
- **Padding box: The padding sits between the border and the content area and is used to push the content away from the border.**
- **Border box: The border is drawn between the margin and the padding of a box.**
- **Margin box: The margin is an invisible space around your box. It pushes other elements away from the box.**

---

## JavaScript Arrays. Operators and Expressions. Conditionals. Loops

---

- What *data types* can you store inside of an *Array*? **strings, numbers, objects, and even other arrays. These can be mixed within a single array.**
- Is the *people* array a valid JavaScript array? If so, how can I access the values stored? If not, why? **Yes, it's a multidimennsional array. Multidimensional array items can be accessed by a double set of `[]` to specify the indiex location.**

 `const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];`

- List five shorthand operators for assignment in javascript and describe what they do.

- **`+=` sets the variable to the value of adding (or concatenating) the variable's original value + an additional value**
- **`*=` sets the variable to the value of multiplying the variable's original value + an other value**
- **`%=` sets the variable to the value of the remainder value after dividing variable's original value by an other value**
- **`<<=` The left shift assignment operator (<<=) moves the specified amount of bits to the left and assigns the result to the variable. ([from MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Left_shift_assignment))**
- **`&&=` The logical AND assignment (x &&= y) operator only assigns if x is truthy. ([from MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND_assignment))**

- Read the code below and evaluate the last *expression* and explain what the result would be and why.

 `let a = 10;`
 `let b = 'dog';`
 `let c = false;`

 `// evaluate this`
 `(a + c) + b;`

 **the result is `10dog`. The boolean value of false is not added to the string because it's not converted to a string variable first.**

- Describe a real world example of when a conditional statement should be used in a JavaScript program. **verifying a customer is old enough to buy alcohol by evaluating their birthdate vs the current date.**
- Give an example of when a *Loop* is useful in JavaScript. **use a counter to verify a job/task executes the correct number of times (or not at all).**

---

## Things I want to know more about

- I'm so lost on CSS. Neeing to know more != wanting to know more.
