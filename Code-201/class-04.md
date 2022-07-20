# HTML Links, JS Functions, and Intro to CSS Layout

## Learn HTML

### Creating Hyperlinks

> Hyperlinks allow us to link documents to other documents or resources, link to specific parts of documents, or make apps available at a web address. ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#what_is_a_hyperlink))
> A basic link is created by wrapping the text or other content inside an `<a>` element and using the href attribute, also known as a Hypertext Reference, or target, that contains the web address. E.g. `<a href="https://www.mozilla.org/en-US/">the Mozilla homepage</a>`. ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#anatomy_of_a_link))

The `title`  attribute adds additional information about the link. Embed an `<img>` block-level element insisde `<a></a>` to set a image to a link.

> Document fragments:  It's possible to link to a specific part of an HTML document, known as a document fragment, rather than just to the top of the document. ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#document_fragments))

Absolute vs Relative URLs:

> - absolute URL: Points to a location defined by its absolute location on the web, including protocol and domain name. An absolute URL will always point to the same location, no matter where it's used.
> - relative URL: Points to a location that is relative to the file you are linking from. A relative URL will point to different places depending on the actual location of the file you refer from.
> - ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#absolute_versus_relative_urls))

Best Practices:

> - Use clear wording. Make your links accessible to all readers, regardless of their current context and which tools they prefer.
> - Screen reader users like jumping around from link to link on the page, and reading links out of context.
> - Search engines use link text to index target files, so it is a good idea to include keywords in your link text to effectively describe what is being linked to.
> - Visual readers skim over the page rather than reading every word, and their eyes will be drawn to page features that stand out, like links.
> - ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#link_best_practices))

Leave signposts when linking to non-HTML sources. Use the `download` attribute when linking to a download.

Email links: e.g. `mailto:nowhere@mozilla.org?cc=nobody@mozilla.org&subject=This%20is%20the%20subject`

---

1. To create a basic link, we wrap text or other content inside what element? **The `<a>` element.**
2. The href attribute contains what information? **Hypertext Reference, or target. This is the web address.**
3. What are some ways we can ensure links on our pages are accessible to all readers?

  > - **Screen reader users like jumping around from link to link on the page, and reading links out of context.**
  > - **Search engines use link text to index target files, so it is a good idea to include keywords in your link text to effectively describe what is being linked to.**
  > - **Visual readers skim over the page rather than reading every word, and their eyes will be drawn to page features that stand out, like links.**

---

## CSS Layout

### CSS Layout: Normal Flow

Normal flow is the default way that webpage elements are laid out if their layout hasn't been changed. *"Starting with a solid, well-structured document that's readable in normal flow is the best way to begin any webpage. It ensures that your content is readable even if the user's using a very limited browser or a device such as a screen reader that reads out the content of the page."* ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow))

Default layout:

> - The process begins as the boxes of individual elements are laid out in such a way that any padding, margin, or border they happen to have is added to their content. This is what we call the **box model**.
> - A block level element's content fills the available inline space of the parent element containing it and grows along the block dimension to accommodate its content.
> - The size of Inline elements is just the size of their content. You can't set width or height on inline elements — they just sit inside the content of block level elements.
> - If you want to control the size of an inline element in this manner, you need to set it to behave like a block level element (e.g., with display: block; or display: inline-block;, which mixes characteristics from both).
> - ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow#how_are_elements_laid_out_by_default))

### CSS Layout: Positioning

> - Positioning allows you to take elements out of normal document flow and make them behave differently. Positioning allows us to produce interesting results by overriding normal document flow. ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning))

Types of positioning:

- Static positioning: Static positioning is the default that every element gets.
- Relative positioning: Once the positioned element has taken its place in the normal flow, its final position can be modified.
- Absolute positioning: Absolute positioning brings very different results. But no one knows what they are.
- Fixed positioning: Similar to aboslute positioning except while absolute positioning fixes an element in place relative to its nearest positioned ancestor, fixed positioning usually fixes an element in place relative to the visible portion of the viewport.
- Sticky positioning: a hybrid between relative and fixed position. Frequently used to make scrolling indexes on a page.

---

1. What is meant by “normal flow”? **It's the default way that webpage elements are laid out if their layout hasn't been changed**
2. What are a few differences between *block-level* and *inline* elements? **A block level element's content fills the available inline space of the parent element. The size of Inline elements is just the size of their content.**
3. ___ positioning is the default for every html element. **Static**
4. Name a few advantages to using absolute positioning on an element. **An absolutely positioned element no longer exists in the normal document flow. Instead, it sits on its own layer separate from everything else.**
5. What is a key difference between fixed positioning and absolute positioning? **fixed positioning usually fixes an element in place relative to the visible portion of the viewport.**

---

## Learn JavaScript

### Functions - Reusable Blocks of Code

Functions allow you to store a piece of code that does a single task inside a defined block, and then call that code whenever you need it using a single short command. ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions))

---

1. Describe the difference between a function declaration and a function invocation. **A function declaration specifies the code, variables, logic, etc. of the function. A function invocation calls the function from elsewhere in the coebase to use it's functionity.**
2. What is the difference between a parameter and an argument? **A parameter is a data element specified when invoking a function. Parameters are sometimes called arguments, properties, or even attributes.**

---

## Misc

### 6 Reasons for Pair Programming aka "two heads are better than one”

Two roles:

- Driver: types the code, the only hands-on person
- Navigator: guides the driver, but does not provide any direct input into the computer

Why? Pair programming actively requires Listening, Speaking, Reading, and Writing skills. These are fundemental for learning new languages.

6 Reasons:

- Greater Efficiency
- Engaged Collaboration
- Learning from Fellow Students
- Social Skills
- Job Interview Readiness
- Work Environment Readiness

---

1. Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.

    - Engage Collaboration: **It is harder to procrastinate or get off track when someone else is relying on you to complete the work.**
    - Job Interview Readiness: **Improve my ability to collaborate with teammates vs putting my head down and going to town on my own.**

---
