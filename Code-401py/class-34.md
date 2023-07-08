# API Deployment (and also supposedly Back End Deployment)

## Reading

- [Django Settings Best Practices](https://djangostars.com/blog/configuring-django-settings-best-practices/)

- Problems when managing Django settings:
  - Different environments
  - Sensitive data
  - Sharing settings between team members
  - Django settings are a Python code
- Popular approaches for setting Django configurations:
  - settings_local.py
    - pros:
      - secrets not in VCS
    - cons:
      - settings_local.py is not in VCS, so you can lose some of your Django environment settings.
      - The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.
      - You need to have settings_local.example (in VCS) to share the default Django configurations for developers.
  - Separate settings file for each environment
    - pros:
      - All environments are in VCS.
      - It’s easy to share settings between developers.
    - cons:
      - You need to find a way to handle secret passwords and tokens.
      - “Inheritance” of settings can be hard to trace and maintain.
  - Environment variables
    - pros:
      - Django config is separated from code.
      - Environment parity – you have the same code for all environments.
      - No inheritance in settings, and cleaner and more consistent code.
      -There is a theoretical grounding for using Django environment variables – 12 Factors.
    - cons:
      - You need to handle sharing default config between developers.
  - 12 Factors
    - Each point describes a recommended way to implement a specific aspect of the project.
    - Its main rule is to store configuration in the environment.
    - [12factor.net](https://12factor.net/)
  - django-environ
    - Based on the above, Django env variables are the perfect place to store settings.
    - Writing code using os.environ could be tricky sometimes and require additional effort to handle errors. It’s better to use django-environ instead.
  - Setting Structure
    - Instead of splitting settings by environments, you can split them by the source: Django, third- party apps (Celery, DRF, etc.), and your custom settings.
  - Naming Conventions
    - follow these simple rules for our custom (project) settings:
      - Give meaningful names to your settings.
      - Always use the prefix with the project name for your custom (project) settings.
      - Write descriptions for your settings in comments.
  - Django Settings: Best practices
    - Keep settings in environment variables.
    - Write default values for production configuration (excluding secret keys and tokens).
    - Don’t hardcode sensitive settings, and don’t put them in VCS.
    - Split settings into groups: Django, third-party, project.
    - Follow naming conventions for custom (project) settings.
  - [django-environ documentation](https://django-environ.readthedocs.io/en/latest/)

## Bookmark and Review

- [White Noise](http://whitenoise.evans.io/en/stable/)

  - WhiteNoise allows your web app to serve its own static files, making it a self-contained unit that can be deployed anywhere without relying on nginx, Amazon S3 or any other external service.
  - WhiteNoise works with any WSGI-compatible app but has some special auto-configuration features for Django.

- [CORS](https://en.m.wikipedia.org/wiki/Cross-origin_resource_sharing)

  - Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources on a web page to be accessed from another domain outside the domain from which the first resource was served.
  - CORS defines a way in which a browser and server can interact to determine whether it is safe to allow the cross-origin request.

## Reading Questions

- What are the key principles to follow when organizing and configuring Django settings for a project, according to the “Django Settings Best Practices” reading?

- How does the White Noise library contribute to the efficient serving of static files in a Django application, and what are the steps to integrate it into a project?

- What is the purpose of Cross-Origin Resource Sharing (CORS) in web applications, and how can it be implemented and configured in a Django project to control access to resources?
