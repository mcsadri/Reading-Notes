# Intro to Django

## Reading

### [Getting started with Django](https://www.djangoproject.com/start/)

- Object-relational mapper
- To design URLs for an application, you create a Python module called a URLconf. Like a table of contents for your app, it contains a simple mapping between URL patterns and your views.
- Templates are flexible and highly extensible, allowing developers to augment the template language as needed.
- Can render forms as HTML to create and update data.
- Has full-featured and secure authentication system.
- Includes an automatic admin interface.
- full support for translating text into different languages, plus locale-specific formatting of dates, times, numbers, and time zones.
- Multiple security protections

### [How Django Works Behind the Scenes](https://wsvincent.com/how-django-works-behind-the-scenes/)

- Django is an open-source, Python-based web framework
- major releases every nine months, minor security releases almost monthly
- Django Software Foundation

### [What is Tailwind CSS?](https://blog.hubspot.com/website/what-is-tailwind-css)

## Bookmark and Review

- [What is Django](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Introduction)
  - Django is a high-level Python web framework that enables rapid development of secure and maintainable websites
  - Web frameworks often refer to themselves as "opinionated" or "unopinionated".
    - Opinionated frameworks are those with opinions about the "right way" to handle any particular task.
    - Unopinionated frameworks, by contrast, have far fewer restrictions on the best way to glue components together to achieve a goal, or even what components should be used.
    - Django is "somewhat opinionated", and hence delivers the "best of both worlds".
  - Sending the request to the right view (urls.py)
    - A URL mapper is typically stored in a file named urls.py.
  - Handling the request (views.py)
    - Views are the heart of the web application, receiving HTTP requests from web clients and returning HTTP responses.
    - Views are usually stored in a file called views.py.
  - Defining data models (models.py)
    - Django web applications manage and query data through Python objects referred to as models.
    - Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, etc.
  - Querying data (views.py)
    - The Django model provides a simple query API for searching the associated database. This can match against a number of fields at a time using different criteria (e.g. exact, case-insensitive, greater than, etc.), and can support complex statements.
  - Rendering data (HTML templates)
    - Template systems allow you to specify the structure of an output document, using placeholders for data that will be filled in when a page is generated. Templates are often used to create HTML, but can also create other types of document.
  - Other features/abilities with Django:
    - Forms
    - User auth and permissions
    - Caching
    - Admin site
    - Serializing data

- [First Django App - Part 1](https://docs.djangoproject.com/en/4.1/intro/tutorial01/)

- [First Django App - Part 2](https://docs.djangoproject.com/en/4.1/intro/tutorial02/)

- [Tailwind CSS Django - Flowbite](https://flowbite.com/docs/getting-started/django/)

## Reading Questions

- What are the key components of the Django framework, and how do they contribute to building a web application?
  - the core Django framework can be seen as an MVC architecture. It consists of:
    - object-relational mapper (ORM) that mediates between data models (defined as Python classes) and a relational database ("Model")
    - a system for processing HTTP requests with a web templating system ("View")
    - a regular-expression-based URL dispatcher ("Controller")
    - [Wikipedia](https://en.wikipedia.org/wiki/Django_(web_framework)#Components)

- Explain the role of Django’s MTV (Model-View-Template) architecture and how it handles a typical web request-response cycle.
  - Django is based on MVT (Model-View-Template) architecture. MVT is a software design pattern for developing a web application.
    - **Model**: The model is going to act as the interface of your data. It is responsible for maintaining data. It is the logical data structure behind the entire application and is represented by a database (generally relational databases such as MySql, Postgres).
    - **View**: The View is the user interface — what you see in your browser when you render a website. It is represented by HTML/CSS/Javascript and Jinja files.
    - **Template**: A template consists of static parts of the desired HTML output as well as some special syntax describing how dynamic content will be inserted.
    - [GeeksForGeeks](https://www.geeksforgeeks.org/django-project-mvt-structure/)

- What is the purpose of Tailwind CSS, and how does it differ from Bootstrap CSS?
  - "Tailwind CSS is a utility-first CSS framework designed to enable users to create applications faster and easier. You can use utility classes to control the layout, color, spacing, typography, shadows, and more to create a completely custom component design — without leaving your HTML or writing a single line of custom CSS."
    - write less custom CSS
    - keep CSS files small
    - no need to invent class names
    - can make safer changes
  - Tailwind doesn’t offer fully styled components like buttons, dropdowns, and navbars. Instead, it offers utility classes so you can create your own reusable components.
    - it provides a lot more flexibility and control over what your application looks like than other CSS frameworks. This can enable you to create a more unique site.
