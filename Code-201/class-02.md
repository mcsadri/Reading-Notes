# Basics of HTML, CSS & JavaScript

## HTML Text Fundamentals: Advanced Text Formatting

### Description Lists

HTML has a third type of marking up lists in addition to Unordered and Ordered: Description Lists

> Description lists use a different wrapper than the other list types — `<dl>`; in addition each term is wrapped in a `<dt>` (description term) element, and each description is wrapped in a `<dd>` (description definition) element. [from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#description_lists)

Multiple `<dd>` tags can be used in conjunction with one `<dt>` tag.

### Quotations

HTML can also mark up quotations:

Blockquotes:
>If a section of block level content (be it a paragraph, multiple paragraphs, a list, etc.) is quoted from somewhere else, you should wrap it inside a `<blockquote>` element to signify this, and include a URL pointing to the source of the quote inside a `cite` attribute  [from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#quotations)

Inline quotes:
> Inline quotations work in exactly the same way, except that they use the `<q>` element. [from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#quotations)

Citations:

- The `cite` attribute allows for providing an attribution/citation in the HTML, but by default this information is not rendered on the webpage.

- > However there is a `<cite>` element, but this is meant to contain the title of the resource being quoted, e.g. the name of the book. There is no reason, however, why you couldn't link the text inside `<cite>` to the quote source. [from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#quotations)

### Abbreviations

The `<abbr>` tag is used to wrap an abbreviation and provide the full term in a tool-tip. The full term is included in the `title` attribute.

### Contact Details

> HTML has an element for marking up contact details — <address>. The <address> element should only be used to provide contact information for the document contained with the nearest <article> or <body> element. ([from MDN web](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#marking_up_contact_details))