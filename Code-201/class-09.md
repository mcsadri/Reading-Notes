# Forms and Events

## HTML Forms

### Your First Web Form

#### Web forms. What are they? How do they even work?

> - Web forms are one of the main points of interaction between a user and a web site or application.
> - Forms allow users to enter data, which is generally sent to a web server for processing and storage , or used on the client-side to immediately update the interface in some way.
> - A web form's HTML is made up of one or more **form controls**, plus some additional elements to help structure the overall form — they are often referred to as HTML forms.
> - ([from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form#what_are_web_forms))

#### Designing a Form

Keep it simple and stay focused.

#### Implementing a Form with HTML

> - All forms start with a `<form>` element.
> - Best practice to include the `action` and `method` attributes.
>   - The `action` attribute defines the location (URL) where the form's collected data should be sent when it is submitted.
>   - The `method` attribute defines which HTTP method to send the data with (usually `get` or `post`).
> - The data entry portion of the form contains three text fields, each with a corresponding `<label>`: `<label>`, `<input>`, and `<textarea>`
> - The use of the for attribute on all `<label>` elements, which takes as its value the id of the form control with which it is associated — this is how you associate a form control with its label.
> - On the `<input>` element, the most important attribute is the `type` attribute. It defines the way the `<input>` element appears and behaves.
> - The `<input>` tag is an empty element, meaning that it doesn't need a closing tag. But `<textarea>` is not an empty element, meaning it should be closed with the proper ending tag
> - The `<button>` element also accepts a type attribute — this accepts one of three values: `submit`, `reset`, or `button`.
>   - A `submit` button (the default value) sends the form's data to the web page defined by the action attribute of the `<form>` element.
>   - A `reset` button resets all the form widgets to their default value immediately.
>   - A click on a `button` button does nothing! Useful for building custom buttons — their functionality is defined with JavaScript.
> - ([from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form#active_learning_implementing_our_form_html))

#### Sending form data to your web server

> - The `<form>` element defines where and how to send the data thanks to the `action` and `method` attributes.
> - We provide a name attribute for each form control.
>   - The names are important on both the client- and server-side. The form data is sent to the server as name/value pairs.
> - To name the data in a form, you need to use the `name` attribute on each form widget that will collect a specific piece of data.
> - ([from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form#sending_form_data_to_your_web_servers))

### How to Structure A Web Form

#### The `<form>` element

> - The `<form`> element formally defines a form and attributes that determine the form's behavior.
> - Each time you want to create an HTML form, you must start it by using this element, nesting all the contents inside.
> - Many assistive technologies and browser plugins can discover `<form>` elements and implement special hooks to make them easier to use.
> - ([from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#the_form_element))

#### The `<fieldset>` and `<legend>` elements

> - The `<fieldset>` element is a convenient way to create groups of widgets that share the same purpose, for styling and semantic purposes.
> - You can label a `<fieldset>` by including a `<legend>` element just below the opening `<fieldset>` tag.
> - The text content of the `<legend>` formally describes the purpose of the `<fieldset>` it is included inside.
> - Many assistive technologies will use the `<legend>` element as if it is a part of the label of each control inside the corresponding `<fieldset>` element.
> - Each time you have a set of radio buttons, you should nest them inside a `<fieldset>` element.
> - The `<fieldset>` element is one of the key elements for building accessible forms
>   - Each time you build a form, try to listen to how a screen reader interprets it. If it sounds odd, try to improve the form structure.
> - ([from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#the_fieldset_and_legend_elements))

#### The `<label>` element

> - The `<label>` element is the formal way to define a label for an HTML form widget.
>   - This is the most important element if you want to build accessible forms
> - Another advantage of properly set up labels is that you can click or tap the label to activate the corresponding widget.
> - you can put multiple labels on a single widget, but this is not a good idea as some assistive technologies can have trouble handling them.
>   - In the case of multiple labels, you should nest a widget and its labels inside a single `<label>` element.
> - ([from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#the_label_element))

#### Common HTML structures used with forms

> - It's common practice to wrap a label and its widget with a `<li>` element within a `<ul>` or `<ol>` list. `<p>` and `<div>` elements are also commonly used.
>   - Lists are recommended for structuring multiple checkboxes or radio buttons.
> - In addition to the `<fieldset>` element, it's also common practice to use HTML titles (e.g. `<h1>`, `<h2>`) and sectioning (e.g. `<section>`) to structure complex forms.
> - Each separate section of functionality should be contained in a separate `<section>` element, with `<fieldset>` elements to contain radio buttons.
> - ([from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#common_html_structures_used_with_forms))

---

1. Why are forms so important in web development? **Web forms are one of the main points of interaction between a user and a web site or application.**
2. When designing a form, what are some key things to keep in mind when it comes to user experience? **Keep it simple and stay focused: ask only for the data you absolutely need. Designing a quick mockup will help you to define the right set of data you want to ask your user to enter.**
3. List 5 form elements and explain their importance.

- `<form>`: formally defines a form
- `<label>`: represents a caption for an item in a user interface.
- `<input>`:  is used to create interactive controls for web-based forms in order to accept data from the user
- `<textarea>`: represents a multi-line plain-text editing control text box
- `<button>`: an interactive element activated by a user to perform a programmable action

---

## Learn JavaScript

### Introduction to Events

> - Events are actions or occurrences that happen in the system you are programming, which the system tells you about so your code can react to them.


---

1. How would you describe events to a non-technical friend?
2. When using the `addEventListener()` method, what 2 arguments will you need to provide?
3. Describe the event object. Why is the target within the event object useful?
4. What is the difference between event bubbling and event capturing?

---
