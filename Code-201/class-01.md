# Code 201 - Class 01

These topics are an introductory description of how the web, HTML, JavaScript, etc. work in order to provide a ground-level context for learning front-end software development.

## Getting Started

### Website Design and Process

High level design process steps:

- Planning:
  - What is your website about, or what will it do?
  - What information are you using/sharing?
  - What will it look like?
- Sketch a wireframe design
- Choose the assets to be used:
  - Text
  - Font
  - Themes/Colors
  - Images

### How the Web Works

#### Cat & dogs, birds & the bees, clients & servers

- Clients (e.g. personal computer, mobile phone, etc.) are internet connected devices with software used to submit requests for data or to interact with data on servers
- Servers are remote computer that server webpages, apps, etc. The server responds and send the requested data for the client

#### Other components:

- Internet/network connection
- TCP/IP
- DNS
- HTTP
- Component files
  - Code files
  - Assets

#### Other concepts:

- Order of parsing component files
- What is DNS?
- How are packets?

### What is JavaScript?

JavaScript is:

- a powerful programming language
- versatile & beginner-friendly
- but also able to create games, animations, database driven apps
- relatively compact
- widely supported with
  - browser APIs
  - third-party APIs
  - third-party frameworks & libraries

#### Langurage Basics

##### Variables

Variables are containers to hold data values. Types of variables include:

- String
- Number
- Boolean
- Array
- Object

##### Comments

Comments are used to insert snippets of text in your code that are ignored during code execution.

---
Reading question/task answers:

1. A haiku:

> browser sends request
> servers says yes here's data
> puzzle assembled

2. The following is borrowed from [How the web works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works#order_in_which_component_files_are_parsed)

>The browser parses the HTML file first, and that leads to the browser recognizing any `<link>`-element references to external CSS stylesheets and any `<script>`-element references to scripts.
>
> As the browser parses the HTML, it sends requests back to the server for any CSS files it has found from `<link>` elements, and any JavaScript files it has found from `<script>` elements, and from those, then parses the CSS and JavaScript.
>
> The browser generates an in-memory DOM tree from the parsed HTML, generates an in-memory CSSOM structure from the parsed CSS, and compiles and executes the parsed JavaScript.
>
>As the browser builds the DOM tree and applies the styles from the CSSOM tree and executes the JavaScript, a visual representation of the page is painted to the screen, and the user sees the page content and can begin to interact with it.

3. An easy way to find image assets is search Google Images and download items suitable to the need. It's recommended to use Google's license filter to only search images with a Creative Commons license to avoid copyright violation.
4. When declaring a **string** enclose the value in single-quotes, vs. when declaring a **number** the numeric value does not go in quotes. E.g.

```javascript
let userName = "Thomas";
let userAge = 25;
```

5. Variables are containers to hold data values. Variables are essential in code for referencing, and manipluating information.

---

## Introduction to HTML (I thought I just did this less than 3 weeks ago)

HTML (Hypertext Markup Language) is a programming language that uses **elements** to pieces of text different meaning and function. It tells a web browser how to structure a web page.

### Elements

- An HTML element is comprised of:
  - opening tag
  - content
  - closing tag
  - may also include Attributes
- Elements can be nested within other elements
- Elements are categorized as:
  - either Block-level
  - or Inline
- Empty elements only use a single, opening tag

### Document and website structure

Basic secitons of a HTML document:

- header
- navigation bar
- main content
- footer

HTML layout elements:

- `<main>`
- `<article>`
- `<section>`
- `<aside>`
- `<header>`
- `<nav>`
- `<footer>`

### HTMl Metadata

Information stored in the HTML `<head>` is not displayed. It contains webpage metadata (e.g. title, author, SEO keywords, etc.), primary language, references, and links (including CSS and/or JavaScript).

---
Reading question/task answers:

1. Attributes contain additional information that describe an element. They could assign an element ID, set a color, or provide an href among other possibilities.
2. Most HTML element are structured as: `<opening tag>`content`</closing tag>`. The opening tag may also inlcude one or more attributes.
3. An `<article>` is used to encapsulate a block of related content that's independent of the rest of the page's content. The `<section>` element is used to encapsulate a single component of a webpage's functionality.
4. The HTML elements of a typical webiste include (but not limited to) the following:

  - `<html>`
  - `<head>`
  - `<body>`
  - `<header>`
  - `<nav>`
  - `<main>`
  - `<section>`
  - `<article>`
  - `<footer>`

5. Keyword metadata can help a webpage appear higher in search results performed by search engine via Search Engine Optimization.
6. the `<meta>` tag uses `name` and `content` attributes to define metadata content. (e.g. `<meta name="author" content="Manuch Sadri">`)

---

---
Miscellaneous reading question/task answers:

How to start designing a website:

1. Project ideation
2. What do i want to accomplish?

Semantics:

1. I don't get semantics.
2. I still don't get semantics.

What is JavaScript?

1. It's late and an obvious answer is alluding me right now.
2. Use the `<script>` HTML element to reference an external JavaScript file, or insert JavaScript code into the HTML directly

---

## Things I want to know more about

- nothing yet
