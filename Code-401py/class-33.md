# Authentication & Production Server

## Reading

- [JSON Web Tokens](https://jwt.io/introduction/)

  - JWT: JSON Web Token
    - open standard for securely transmitting data between parties
    - digitally signed: can be verified and trusted
      - When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.
    - can be used in secrtet or with public/private key pair
  - When to use:
    - Authorization
    - Information exchange
  - JWT Structure:
    - Header - the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.
    - Payload - contains the claims. Claims are statements about an entity (typically, the user) and additional data.
      - There are three types of claims:
        - registered
        - public
        - private
    - Signature - used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify that the sender of the JWT is who it says it is.
  - How do JWT work?
    - In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned
    - Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the `Authorization` header using the `Bearer` schema.
    - The server's protected routes will check for a valid JWT in the `Authorization` header, and if it's present, the user will be allowed to access protected resources.
      - If the token is sent in the Authorization header, Cross-Origin Resource Sharing (CORS) won't be an issue as it doesn't use cookies.
    - with signed tokens, all the information contained within the token is exposed to users or other parties, even though they are unable to change it.
  - Why use JWT?
    - JSON is less verbose thant XML and SAML
    - SWT can only be symmetrically signed by a shared secret using the HMAC algorithm
    - JSON parsers are common in most programming languages because they map directly to objects

- [DRF JWT Authentication](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)

- [Django Runserver Is Not Your Production Server](https://build.vsupalov.com/django-runserver-in-production/)

## Videos

- [JWT with DRF](https://www.youtube.com/watch?v=Fhcn2qx-4VQ)

## Bookmark & Review

- [Gunicorn](https://gunicorn.org/)

- [Django Migrations Primer](https://realpython.com/django-migrations-a-primer/)

## Reading Questions

- What is the primary purpose of JSON Web Tokens (JWTs) and how do they work in terms of encoding and decoding data?

- How does JWT Authentication integrate with Django REST Framework to secure API endpoints, and what are the key components involved in this process?

- Why is Django’s built-in runserver not suitable for production environments, and what are some alternative server options that should be considered for deploying a Django application?
