# Permissions & Postresql

## Reading

- [DRF Permissions](https://www.django-rest-framework.org/api-guide/permissions/)
  - Permissions:
    - Permission checks are always run at the very start of the view, before any other code is allowed to proceed.
      - Permission checks will typically use the authentication information in the `request.user` and `request.auth` properties to determine if the incoming request should be permitted.
    - Permissions in REST framework are always defined as a list of permission classes.
    - If any permission check fails, an `exceptions.PermissionDenied` or `exceptions.NotAuthenticated` exception will be raised, and the main body of the view will not run.
      - When the permission checks fail, either a "403 Forbidden" or a "401 Unauthorized" response will be returned
    - Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.
      - Object level permissions are run by REST framework's generic views when .get_object() is called.
    - The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting.
      - You can also set the authentication policy on a per-view, or per-viewset basis, using the APIView class-based views.
    - API Reference:
      - AllowAny
      - IsAuthenticated
      - IsAdminUser
      - IsAuthenticatedOrReadOnly
      - DjangoModelPermissions
      - DjangoModelPermissionsOrAnonReadOnly
      - DjangoObjectPermissions
    - Custom Permissions
      - To implement a custom permission, override `BasePermission` and implement either, or both, of the following methods:
        - `.has_permission(self, request, view)`
        - `.has_object_permission(self, request, view, obj)`
      - The methods should return `True` if the request should be granted access, and `False` otherwise.
      - Custom permissions will raise a `PermissionDenied` exception if the test fails.
    - Overview:
      - REST framework offers three different methods to customize access restrictions on a case-by-case basis:
        - `queryset`/`get_queryset()`
        - `permission_classes`/`get_permissions()`
        - `serializer_class`/`get_serializer()`
    - Numerous third party packages also available

- [Review SQL Prework](https://codefellows.github.io/common_curriculum/prework/SQL)

## Bookmark and Review

- [Classy Django REST](http://www.cdrf.co/)

- [DRF Generic Views](https://www.django-rest-framework.org/api-guide/generic-views/)

## Reading Questions

- What are the key components and purpose of Django Rest Framework (DRF) permissions, and how do they help in securing an API?

- In SQL, what is the purpose of the SELECT statement, and how would you use it to retrieve all columns from a table called ‘employees’?

- Can you explain the role of DRF Generic Views and provide examples of their usage in building a RESTful API?
