# Django Custom User

## Reading

### - [Django Custum User Model](https://learndjango.com/tutorials/django-custom-user-model)

### - [DjangoX](https://github.com/wsvincent/djangox)

## Videos

### - [Creating a Custom User Moel](https://www.youtube.com/watch?v=eCeRC7E8Z7Y&t=59s)

### - [Abstract User, User Profile and Signals in Django](https://www.youtube.com/watch?v=EudKs1HPUfE)

## Bookmark and Review

### - [Substituting a custom User model](https://docs.djangoproject.com/en/3.0/topics/auth/customizing/#auth-custom-user)

## Reading Questions

- What are the key benefits of using a Django Custom User Model, and how does it differ from the default Django User Model?
  - Key benefits:
    - Flexibility
    - Scalability
    - Maintainability
  - Key differences:
    - Authentication fields
    - Extensibility
    - Database schema control

- Explain the process of creating and implementing a Custom User Model in Django, including the necessary changes to settings.py and the required model fields.
  - Create a new Django project or navigate to an existing project.
  - Inside the django project create a new app
  - Add/open models.py
  - Import modules
  - Add new custom User model class
  - Inside settings.py, update the AUTH_USER_MODEL
  - Run makemigrations and migrate
  - Import customer user model in views, etc.

- What is DjangoX and how does it complement or extend the functionality of Django? Provide an example use case for incorporating DjangoX in a project.
  - Djangox helps developers launch new Django projects quickly with a complete user authentication flow, custom user model, social authentication options, and more.
  - It comes with a custom user model by default, email/password authentication.
  - It's fully extendable with social authentication like Gmail, Facebook, and more
