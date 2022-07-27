# JavaScript Object Literals, the DOM

## JavaScript Object Basics

---

1. How would you describe an object to a non-technical friend you grew up with?
2. What are some advantages to creating object literals?
3. How do objects differ from arrays?
4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
5. Evaluate the code below. What does the term **this** refer to and what is the advantage to using **this**?

``` javascript
const dog = {
  name: 'Spot',
  age: 2,
  color: 'white with black spots',
  humanAge: function (){
    console.log(`${this.name} is ${this.age*7} in human years`);
  }
}

```

---

## Introduction to the DOM

The **Document Object Model** (*DOM*) is the data representation of the objects that comprise the structure and content of a document on the web. ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction))

### But what is it?

>- The Document Object Model (DOM) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content.
> - A web page is a document that can be either displayed in the browser window or as the HTML source.
> - With the DOM's object-oriented representation of the web page, it can be modified with a scripting language such as JavaScript.
> - The properties, methods, and events available for manipulating and creating web pages are organized into objects. e.g. the document object that represents the document itself, any table objects that implement the HTMLTableElement DOM interface for accessing HTML tables, and so forth, are all objects.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#what_is_the_dom))

### DOM and JavaScript

> - The DOM is not a programming language, but without it, the JavaScript language wouldn't have any model or notion of web pages, HTML documents, SVG documents, and their component parts.
> - **All** other elements in a document (e.g.  head, tables, table headers, text within the table cells, etc.) are parts of the document object model for that document.
> - The DOM is not part of the JavaScript language, but is instead a Web API used to build websites.
> - The DOM is independent of any particular programming language.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#dom_and_javascript))

### Accessing the DOM

- JavaScript's API is all that's needed to manipulate the document with a script.
- With the API you can use the `document` or `window` objects to manipulate the document itself, or any of the various elements in the web page.
- It's best practice to not mix the HTML structure of the document/page with the JavaScript manipulation of the DOM. The JavaScript will be grouped together, separeate from the HTML.
- ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#accessing_the_dom))

### Fundamental Data Types

| Data type (Interface) | Description |
| --- | --- |
| Document | the root document object |
| Node | Every object located within a document is a node of some kind |
| Element | An element or a node of type element returned by a member of the DOM API. In an HTML document, elements are further enhanced by the HTML DOM API's HTMLElement interface as well as other interfaces describing capabilities of specific kinds of elements. |
| NodeList | A nodeList is an array of element |
| Attr | When an attribute is returned by a member  it is an object reference that exposes a special (albeit small) interface for attributes. |
| NamedNodeMap | A namedNodeMap is like an array, but the items are accessed by name or index |

([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#fundamental_data_types))

### DOM Interfaces

#### Interfaces and Objects

> - Many objects borrow from several different interfaces:
>   - The table object, for example, implements a specialized `HTMLTableElement` interface
>     - which includes such methods as `createCaption` and `insertRow`
>   - But since it's also an HTML element
>     - `table` implements the `Element` interface described in the DOM [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element) Reference chapter
>   - since an HTML element is also, as far as the DOM is concerned, a node in the tree of nodes that make up the object model for an HTML or XML page
>     - the table object also implements the more basic Node interface, from which Element derives.
>   - When you get a reference to a table object, as in the following example, you routinely use all three of these interfaces interchangeably on the object, perhaps without knowing it.
> - ([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#interfaces_and_objects))

#### Core interfaces in the DOM

> - The `document` and `window` objects are the objects whose interfaces you generally use most often in DOM programming. E.g.:
>   - the `window` object represents something like the browser
>   - the `document` object is the root of the document itself
> - `Element` inherits from the generic `Node` interface, and together these two interfaces provide many of the methods and properties you use on individual elements

> - Some common APIs in web and XML page scripting using the DOM.
>   - document.querySelector(selector)
>   - document.querySelectorAll(name)
>   - document.createElement(name)
>   - parentNode.appendChild(node)
>   - element.innerHTML
>   - element.style.left
>   - element.setAttribute()
>   - element.getAttribute()
>   - element.addEventListener()
>   - window.content
>   - GlobalEventHandlers/onload
>   - window.scrollTo()

([from MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#core_interfaces_in_the_dom))

---

1. What is the DOM? **It's the data representation of the objects that comprise the structure and content of a document on the web. It represents the page so that programs can change the document structure, style, and content.**
2. Briefly describe the relationship between the DOM and JavaScript. **The DOM is not part of the JavaScript language, but is instead a Web API used to build websites. The DOM is independent of any particular programming language.**

---
