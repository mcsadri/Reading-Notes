# APIs

## [API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

1. What does REST stand for?
    1. Representational State Transfer
2. REST APIs are designed around a ____.
    1. open standard
    2. "resources, which are any kind of object, data, or service that can be accessed by the client"
3. What is an identifier of a resource? Give an example.

    > 1. An identifier of a resource is a Uniform Resource Identifier (URI).
    > 2. URI identifies a resource and differentiates it from others by using a name, location, or both.
    > 3. URI contains components like a scheme, authority, path, and query.
    > 4. An example of a URI is ISBN 0-476-35557-4. [hostinger.com](https://www.hostinger.com/tutorials/uri-vs-url#:~:text=URI%20identifies%20a%20resource%20and,a%20domain%20name%20and%20port.)

4. What are the most common HTTP verbs?
    1. The most common operations are `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`.
5. What should the URIs be based on?
    1. "When possible, resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource)." [Organize the API design around resources](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design#organize-the-api-design-around-resources)
6. Give an example of a good URI.
    1. `https://adventure-works.com/orders`
7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
    1. A chatty API is one that exposes a large number of small resources.
    2. Any and every API request imposes load on the web server. An approach is needed to balance the number of total requests vs the size of the requests.
8. What status code does a successful `GET` request return?
    1. "A successful GET method typically returns HTTP status code 200 (OK)."
9. What status code does an unsuccessful `GET` request return?
    1. "If the resource cannot be found, the method should return 404 (Not Found). If the request was fulfilled but there is no response body included in the HTTP response, then it should return HTTP status code 204 (No Content)."
10. What status code does a successful `POST` request return?
    1. "If a POST method creates a new resource, it returns HTTP status code 201 (Created). The URI of the new resource is included in the Location header of the response. The response body contains a representation of the resource."
11. What status code does a successful `DELETE` request return?
    1. "If the delete operation is successful, the web server should respond with HTTP status code 204 (No Content), indicating that the process has been successfully handled, but that the response body contains no further information. If the resource doesn't exist, the web server can return HTTP 404 (Not Found)."

---

## Further Reading & Review

- [RegExr](https://regexr.com/) - cheatsheet
- [RegEx Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
- [RegEx 101](https://regex101.com/)