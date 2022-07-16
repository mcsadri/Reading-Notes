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

#### Usage Notes

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

---

1. Describe the CSS properties of *margin* and *padding* as characters in a story. What is their role in a story titled: “The Box Model”?
2. List and describe the four parts of an HTML elements box as referred to by the *box model*.

---








## Things I want to know more about

- tbd