# Basics of HTML, CSS & JavaScript

HTML, CSS, JavaScript are the three essential layers for a building modern web pages. These notes will provide an introductory review of the basics of each topic.

## HTML Text Fundamentals: Advanced Text Formatting

### Description Lists

HTML has a third type of marking up lists in addition to Unordered and Ordered: Description Lists

> Description lists use a different wrapper than the other list types — `<dl>`; in addition each term is wrapped in a `<dt>` (description term) element, and each description is wrapped in a `<dd>` (description definition) element. ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#description_lists))

Multiple `<dd>` tags can be used in conjunction with one `<dt>` tag.

### Quotations

HTML can also mark up quotations:

Blockquotes:
>If a section of block level content (be it a paragraph, multiple paragraphs, a list, etc.) is quoted from somewhere else, you should wrap it inside a `<blockquote>` element to signify this, and include a URL pointing to the source of the quote inside a `cite` attribute  ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#quotations))

Inline quotes:
> Inline quotations work in exactly the same way, except that they use the `<q>` element. ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#quotations))

Citations:

- The `cite` attribute allows for providing an attribution/citation in the HTML, but by default this information is not rendered on the webpage.

- > However there is a `<cite>` element, but this is meant to contain the title of the resource being quoted, e.g. the name of the book. There is no reason, however, why you couldn't link the text inside `<cite>` to the quote source. ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#quotations))

### Abbreviations

The `<abbr>` tag is used to wrap an abbreviation and provide the full term in a tool-tip. The full term is included in the `title` attribute.

### Contact Details

> HTML has an element for marking up contact details — `<address>`. The `<address>` element should only be used to provide contact information for the document contained with the nearest `<article>` or `<body>` element. ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#marking_up_contact_details))

### Superscript & Subscript

The Superscript `<sup>` and Subscript `<sub>` elements are used for marking up  items like dates, chemical formulae, and mathematical equations so they have the correct formatting and meaning.

### Code

HTML has seversal elements for marking up computer code:

> - `<code>`: For marking up generic pieces of computer code.
> - `<pre>`: For retaining whitespace (generally code blocks)
> - `<var>`: For specifically marking up variable names.
> - `<kbd>`: For marking up keyboard (and other types of) input entered into the computer.
> - `<samp>`: For marking up the output of a computer program.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#representing_computer_code))

### Date & Time

HTML uses the `<time>` element for marking up times and dates in a machine-readable format. For example:

    `<time datetime="2016-01-20">20 January 2016</time>`

---

1. Why is it important to use semantic elements in our HTML? **The meaning of Semantics still doesn't make any sense to me.**
2. How many levels of headings are there in HTML? **6**
3. What are some uses for the `<sup>` and `<sub>` elements? **These are used for providing correct formatting (and meaning) for things like dates, chemical formulae, and mathematical equations.***
4. When using the <abbr> element, what attribute must be added to provide the full expansion of the term? **`title`**

---

## Learn CSS

What if I don't want to?

### Applying CSS to HTML

There are three ways to apply CSS to a webpage:

- External stylesheet
- Internal stylesheet
- Inline styles

### Selectors

- CSS rules use selectors to apply styles to content.
- **Cascade** and **specifity** are used to resolve possible style conflicts.

### Properties and values

In addition to Selectors CSS rules consist of:

- **Properties**: specified which characterisitc of the Selector is to be styled
- **Values**: specifies how to style the characterestic
- these are case-sensative and use a **:** as a seperator
- most use key word and value pairs, but others use Functions, such as `calc()` or `rotate()`

### @rules

> CSS @rules (pronounced "at-rules") provide instruction for what CSS should perform or how it should behave. Some @rules are simple with just a keyword and a value. One common @rule that you are likely to encounter is @media, which is used to create media queries. Media queries use conditional logic for applying CSS styling. ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured#rules))

### Shorthands

> Some properties like font, background, padding, border, and margin are called shorthand properties. This is because shorthand properties set several values in a single line. ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured#shorthands))

### Comments

Comments are used to add non-interpretted/complied explanatory text to code, and/or disable code from being run during code execution. CSS comments begin with `/*` and end with `*/`.

### White Space

Browsers ignore whitespace in CSS when rendering a webpage, but whitespace can be used to improve the readability of the code.

---

1. What are ways we can apply CSS to our HTML? **External, Internal, or Inline***
2. Why should we avoid using inline styles? **It's the least efficient method for maintenance, and it mixes CSS presentional code within the HTML content.**
3. Review the block of code below and answer the following questions:
    1. What is representing the selector? **`h2`**
    2. Which components are the CSS declarations? **`color: black;` and `padding: 5px;`**
    3. Which components are considered properties? **`color` and `padding`**

---

## Learn JavaScript

### JavaScript Basics

---

1. What data type is a sequence of text enclosed in single quote marks? **string**
2. List 4 types of JavaScript operators. **Arithemeitc, Relational, Equality, Assignment***
3. Describe a real world Problem you could solve with a Function. **In a cookbook, *101 Uses for Hard Boiled Eggs*, the instructions of how to hard boil an egg only need to be provided once, and each subsequent recipe can refer back to this initial instruction set.**

---

### Conditionals

---

1. An if statement checks a __ and if it evaluates to ___, then the code block will execute. **false**
2. What is the use of an `else if`? **allows for additional `if` conditions before `else` and/or exiting the conditional**
3. List 3 different types of comparison operators. **Strictly equal, Less than, Greater than or equal to**
4. What is the difference between the logical operator `&&` and `||`? **`AND` vs `OR`**

---

## Things I want to know more about

- I need to figure out semantics