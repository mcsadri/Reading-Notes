# Django CRUD and Forms

## Reading

### [Django Forms](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms)

- Overview
  - An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server.
  - Django Forms provides a framework that lets you define forms and their fields programmatically, and then use these objects to both generate the form HTML code and handle much of the validation and user interaction.

- HTML Forms
  - The form is defined in HTML as a collection of elements inside `<form>…</form>` tags, containing at least one `input` element of `type="submit"`.
  - The field's `type` attribute defines what sort of widget will be displayed.
    - The `name` and `id` of the field are used to identify the field in JavaScript/CSS/HTML, while `value` defines the initial value for the field when it is first displayed.
    - The matching team label is specified using the `label` tag (see "Enter name" above), with a for field containing the `id` value of the associated `input`.
  - The form attributes define the HTTP `method` used to send the data and the destination of the data on the server (`action`):
    - `action`: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
    - `method`: The HTTP method used to send the data: post or get.
      - The `POST` method should always be used if the data is going to result in a change to the server's database, because it can be made more resistant to cross-site forgery request attacks.
      - The `GET` method should only be used for forms that don't change user data (for example, a search form). It is recommended for when you want to be able to bookmark or share the URL.

- Django form handling process
  - the main things that Django's form handling does are:
    - Display the default form the first time it is requested by the user.
    - Receive data from a submit request and bind it to the form.
    - Clean and validate the data.
    - If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.
    - If all data is valid, perform required actions (such as save the data, send an email, return the result of a search, upload a file, and so on).
    - Once all actions are complete, redirect the user to another page.

- Form and function view
  - Form
    - The `Form` class is the heart of Django's form handling system.
  - Declaring a form
    - The declaration syntax for a `Form` is very similar to that for declaring a `Model`, and shares the same field types (and some similar parameters).
    - Form data is stored in an application's forms.py file, inside the application directory.
  - Form fields
    - There are many other types of form fields, which you will largely recognize from their similarity to the equivalent model field classes.
  - Validation
    - The easiest way to validate a single field is to override the method `clean_<fieldname>()` for the field you want to check.
    - If a value falls outside our range we raise a `ValidationError`, specifying the error text that we want to display in the form if an invalid value is entered.
    - There are numerous other methods and examples for validating forms in [Form and field validation](https://docs.djangoproject.com/en/4.0/ref/forms/validation/) (Django docs).
  - URL configuration
    - ¯\\_(ツ)_/¯
  - View
    - the view has to render the default form when it is first called and then either re-render it with error messages if the data is invalid, or process the data and redirect to a new page if the data is valid.
    - For forms that use a `POST` request to submit information to the server, the most common pattern is for the view to test against the `POST` request type (`if request.method == 'POST':`) to identify form validation requests and `GET` (using an `else` condition) to identify the initial form creation request.
      - If you want to submit your data using a `GET` request, then a typical approach for identifying whether this is the first or subsequent view invocation is to read the form data (e.g. to read a hidden value in the form).
  - The template
    - Add the {% csrf_token %} to every Django template you create that uses `POST` to submit data. This will reduce the chance of forms being hijacked by malicious users.
  - Other ways of using form template variable
    - When using `{{ form.as_table }}` each field is rendered as a table row. You can also render each field as a list item (using `{{ form.as_ul }}`) or as a paragraph (using `{{ form.as_p }}`).
    - It is also possible to have complete control over the rendering of each part of the form, by indexing its properties using dot notation.

- ModelForms
  - class ModelForm
    - Django provides a helper class that lets you create a Form class from a Django model

## Bookmark & Review

- [Django Templates](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Home_page)

- [Django Views](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Generic_views)

## Reading Questions

- How do Django Forms facilitate user input handling, and what are some key components of creating a form using the Django framework?
  - Django Forms provides a framework that lets you define forms and their fields programmatically, and then use these objects to both generate the form HTML code and handle much of the validation and user interaction.
  - The form is defined in HTML as a collection of elements inside `<form>…</form>` tags, containing at least one `input` element of `type="submit"`.

- Explain the purpose of Django Templates in web development and describe how template inheritance can be utilized to improve code reusability and maintainability.
  - Being a web framework, Django needs a convenient way to generate HTML dynamically. The most common approach relies on templates. A template contains the static parts of the desired HTML output as well as some special syntax describing how dynamic content will be inserted [djangoproject.com](https://docs.djangoproject.com/en/4.2/topics/templates/)

- Describe the function of Django Views in handling HTTP requests, and outline the differences between function-based views and class-based views.
  - In the Django framework, views are Python functions or classes that receive a web request and return a web response. The response can be a simple HTTP response, an HTML template response, or an HTTP redirect response that redirects a user to another page. [pluralsight](https://www.pluralsight.com/guides/introduction-to-django-views)
  - Class-based views provide an alternative way to implement views as Python objects instead of functions. They do not replace function-based views, but have certain differences and advantages when compared to function-based views. [Medium.com](https://medium.com/@ksarthak4ever/django-class-based-views-vs-function-based-view-e74b47b2e41b)
