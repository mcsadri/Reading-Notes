# [C.R.U.D.](https://en.wikipedia.org/wiki/C.H.U.D.)

## Reading

### [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

1. In your own words, describe what each group of status code represents:
    1. 100’s = **Informational** codes indicating that the request initiated by the browser is continuing.
    2. 200’s = **Success** codes returned when browser request was received, understood, and processed by the server.
    3. 300’s = **Redirection** codes returned when a new resource has been substituted for the requested resource.
    4. 400’s = **Client error** codes indicating that there was a problem with the request.
    5. 500’s = **Server error** codes indicating that the request was accepted, but that an error on the server prevented the fulfillment of the request. [Kinsta](https://kinsta.com/blog/http-status-codes/)
2. What is a status code 202?
    1. **Accepted** - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future.
3. What is a status code 308?
    1. **Permanent Redirect** status response code indicates that the resource requested has been definitively moved to the URL given by the Location headers.
4. What code would you use if an update didn’t return data to a client?
    1. **204 No Content**: The server successfully processed the request, and is not returning any content.
5. What code would you use if a resource used to exist but no longer does?
    1. **410 Gone**: Indicates that the resource requested was previously in use but is no longer available and will not be available again.
6. What is the ‘Forbidden’ status code?
    1. **403 Forbidden**: The request contained valid data and was understood by the server, but the server is refusing action. This may be due to the user not having the necessary permissions for a resource or needing an account of some sort, or attempting a prohibited action.

## Video

### [Build A REST API With Node.js, Express, & MongoDB - Quick (First 20 minutes)](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
    1. The deployed app will use something other than localhost. And it obfuscates the URL, values, etc. stored in the .env file.
2. What is middleware?
    1. Code that runs when the server gets a request but before it gets passed to the routes.
3. What does `app.use(express.json())` do?
    1. Let's the server accept JSON as a body instead of a post element, get element, etc.
4. What does the `/:id` mean in a route?
    1. It is a parameter accessed by `req.params.id`.
5. What is the difference between `PUT` and `PATCH`?
    1. "**PUT** means replace the entire resource with given data (so null out fields if they are not provided in therequest), while **PATCH** means replace only specified fields." [ServiceNow](https://www.servicenow.com/community/developer-forum/difference-between-put-and-patch-in-rest-api/m-p/1876811)
6. How do you make a default value in a schema?
    1. Use the default property in the schema definition.
7. What does a `500` error status code mean?
    1. Error exists on the server, not the user or client.
8. What is the difference between a status `200` and a status `201`?
    1. 201 means "successfully created an object". 200 means "everything was successful", which is less informative/specific than 201.
