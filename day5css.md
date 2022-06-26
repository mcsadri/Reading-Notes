# CSS And You

## CSS Basics

### Background

Cascading Style Sheets (CSS) are used for modify the appearance of an HTML structured webpage. HTML is used to only provide the structure and the simplest of layout options for a webpage. CSS will be used to modify the appearance attributes of any or every element displayed on-screen.

### Basic Syntax

CSS is a rule-based language — you define the rules by specifying groups of styles that should be applied to particular elements or groups of elements on your web page.

A block of CSS code, or **rule** consists of:

- a selector (e.g. `h`)
- a set of curly brackets `{}` enclosing the
- 1 or more **declarations**
- which consist of a **property** and a **value***
- for example:

```javascript
h1{
        color: red;
        font-size: 25px;
}
```

- a style sheet may contain numerous rules, each applying a set of style declarions to different sections or components of the HTML

### More Info

- CSS modules: there are many things that you could style using CSS, the language is broken down into *modules*
- CSS Specifications: CSS is developed by a group within the W3C called the CSS Working Group
- Browser Support: Browser support status is shown on every MDN CSS property page in a table named "Browser compatibility"

## How to add CSS

When a browser reads a style sheet, it will format the HTML document according to the information in the style sheet. There are three ways of inserting a style sheet:

- External CSS
- Internal CSS
- Inline CSS

### External CSS

- With an external style sheet, you can change the look of an entire website by changing just one file!
- Each HTML page must include a reference to the external style sheet file inside the `<link>` element, inside the head section.
- An external style sheet can be written in any text editor, and must be saved with a .css extension.
- The external .css file should not contain any HTML tags.

### Internal CSS

- An internal style sheet may be used if one single HTML page has a unique style.
- The internal style is defined inside the `<style>` element, inside the head section.

### Inline CSS

- An inline style may be used to apply a unique style for a single element.
- To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.

### CSS Etc

- Multiple Style Sheets: If some properties have been defined for the same selector (element) in different style sheets, the value from the last read style sheet will be used.
- Cascading Order: What style will be used when there is more than one style specified for an HTML element? All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:
  - Inline style (inside an HTML element)
  - External and internal style sheets (in the head section)
  - Browser default
- So, an inline style has the highest priority, and will override external and internal styles and browser defaults.

## Additional information

[MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
[MeyerWebb CSS Tools: Reset CSS](https://meyerweb.com/eric/tools/css/reset/)

  - "The goal of a reset stylesheet is to reduce browser inconsistencies in things like default line heights, margins and font sizes of headings, and so on"
