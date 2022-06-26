# Structure web pages with HTML

## Wireframes

1. What is a wireframe?
- A wireframe is a tool to help a designer play the layout and heirarchy of information of a product

2. Types of wireframes:
- Drawn by hand (e.g. pen & paper, whiteboard, etc.)
- Paper prototypes
- Software-based drawing tools

3. Things to consider:
- Wireframe approached is usually personal preference. For example:
- Wireframe > Interactive Prototype > Visual > Design
- Sketch > Code
- Sketch > Wireframe > Hi-Def Wireframe > Visual > Code
- Sketch > Wireframe > Visual > Code

4. Wireframing tools
- UXPin
- InVision
- Wireframe.cc

### How to make a wireframe

1. Research: know your audience, specify requirements, define use cases, etc.
2. Reference: keep a cheatsheet of goals, requirements, etc. available for handy reference
3. Map user flow
4. Keep it basic. Don't get lost in the details.
5. Add detail and test
6. Transistion to prototype

### Key Principles

1. Clarity: Your wireframe needs to answer the questions of what that site page is, what the user can do there, and if it satisfies their needs.
2. Confidence: Ease of navigation through your site and clear calls-to-action increase user confidence in your brand.
3. Simplicity is key: Too much information, copy, or links, can be distracting to the user and will have a detrimental affect on your users’ ability to achieve their goals.

## HTML Basics

- HTML is a markup language that defines the structure of your content. HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear a certain way, or act a certain way.
- A typical HTML element is comprised of:
  - opening tag
  - closing tag
  - content
  - attributes
    - should have a space between it and the element name (or the previous attribute, if the element already has one or more attributes).
    - should have the attribute name followed by an equal sign
    - should the attribute value wrapped by opening and closing quotation marks.
- Nesting elements (elements placed within the confines of another element)
  - `<p>My cat is <strong>very</strong> grumpy.</p>`
-Empty elements: some elements have no content
  - `<img src="images/firefox-icon.png" alt="My test image">`
- Basic anatomy of an HTML document:
  - `code snippet`
-Blah blah blah

## Semantics

In programming, Semantics refers to the meaning of a piece of code — for example "what effect does running that line of JavaScript have?", or "what purpose or role does that HTML element have" (rather than "what does it look like?".)

### Semantics in JavaScript

In JavaScript, consider a function that takes a string parameter, and returns an <li> element with that string as its textContent. Would you need to look at the code to understand what the function did if it was called build('Peach'), or createLiWithContent('Peach')?

### Semantics in CSS

In CSS, consider styling a list with li elements representing different types of fruits. Would you know what part of the DOM is being selected with div > ul > li, or .fruits__item?

### Semantics in HTML

In HTML, for example, the <h1> element is a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page."

Some of the benefits from writing semantic markup are as follows:

- Search engines will consider its contents as important keywords to influence the page's search rankings (see SEO)
- Screen readers can use it as a signpost to help visually impaired users navigate a page
- Finding blocks of meaningful code is significantly easier than searching through endless divs with or without semantic or namespaced classes
- Suggests to the developer the type of data that will be populated
- Semantic naming mirrors proper custom element/component naming

[HTML Elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)