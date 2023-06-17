# Django Models

## Reading

- [Using Models](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)

- How to define models for a website, what is a model, how is a model declared, what are the main field types, and what are the main ways to access model data?
- Overview:
  - Django web applications access and manage data through Python objects referred to as models.
    - Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.
-Designing the website models:
  - When designing your models, it makes sense to have separate models for every "object" (a group of related information).
  - You might also want to use models to represent selection-list options (e.g. like a drop down list of choices), rather than hard coding the choices into the website itself — this is recommended when all the options aren't known up front or may change.
  - Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).
  - Multiplicities are the numbers on the diagram showing the numbers (maximum and minimum) of each model that may be present in the relationship.
- Model primer:
  - Model definition:
    - Models are usually defined in an application's models.py file.
    - They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata.
  - Fields:
    - A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables.
      - Each database record (row) will consist of one of each field value.
    - Field types are assigned using specific classes, which determine the type of record that is used to store the data in the database, along with validation criteria to be used when values are received from an HTML form (i.e. what constitutes a valid value).
      - The field types can also take arguments that further specify how the field is stored or can be used.
    - The field name is used to refer to it in queries and templates.
      - Fields also have a label, which is specified using the verbose_name argument (with a default value of None).
      - If verbose_name is not set, the label is created from the field name by replacing any underscores with a space, and capitalizing the first letter.
    - Common Field Arguments
    - Common Field Types
    - Metadata:
      - declare model-level metadata for your Model by declaring `class Meta`
      - a useful feature of this metadata is to control the default ordering of records returned when you query the model type
      - Other useful attributes allow you to create and apply new "access permissions" for the model (default permissions are applied automatically), allow ordering based on another field, or to declare that the class is "abstract".
    - Methods:
      - A model can also have methods.
      - Minimally, in every model you should define the standard Python class method `__str__()` to return a human-readable string for each object.
    - Model Management
      - Creating and modifying records
        - To create a record you can define an instance of the model and then call `save()`.
        - You can access the fields in this new record using the dot syntax, and change the values. You have to call `save()` to store modified values to the database.
      - Searching for records
        - You can search for records that match certain criteria using the model's `objects` attribute (provided by the base class).
        - We can get all records for a model as a `QuerySet`, using `objects.all()`.
        - Django's `filter()` method allows us to filter the returned `QuerySet` to match a specified text or numeric field against particular criteria.
        - The fields to match and the type of match are defined in the filter parameter name, using the format: `field_name__match_type` (note the double underscore between `title` and `contains` above).

- [Django Admin](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)

- [Beginner’s Guide to Django - Part 1](https://simpleisbetterthancomplex.com/series/2017/09/04/a-complete-beginners-guide-to-django-part-1.html)

## Bookmark and Review

- [Beginner’s Guide to Django - Part 2](https://simpleisbetterthancomplex.com/series/2017/09/11/a-complete-beginners-guide-to-django-part-2.html)

## Reading Questions

- Explain the purpose and basic structure of Django models. How do they help in creating and managing database schema in a Django application?
  - Models are a core component of the framework's Object-Relational Mapping (ORM) system. They represent the structure and behavior of your application's data and provide a convenient way to interact with the underlying database.
  - Models are used to define the entities and relationships in your application's data domain.

- Describe the primary features and functionality of the Django Admin interface. How can it be customized to suit the specific needs of a project?
  - Automatic generation
  - User auth and permissions
  - Model management
  - Search and filtering
  - Customization
  - Inline editing
  - Actions and batch processing
  - Integration with 3rd-party apps
  - [chatgpt](https://chat.openai.com/share/c0b18ddf-b7d8-4c57-9d1b-a942db6ea445)

- Briefly outline the key components and workflow of a Django application, as discussed in the Beginner’s Guide to Django. How do these components interact with each other to create a functional web application?
