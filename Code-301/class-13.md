# [C.R.U.D. 2](https://www.imdb.com/title/tt0097001/)

## Reading

### [CRUD Basics](https://medium.com/geekculture/crud-operations-explained-2a44096e9c88)

1. Which HTTP method would you use to update a record through an API?
    1. PUT
2. Which REST methods require an ID parameter?
    1. PUT
    2. DELETE

## Video

### [Speed Coding: Building a CRUD API (Watch a Twitch streamer code an Express API in 20 minutes!)](https://www.youtube.com/watch?v=EzNcBhSv1Wo)

1. What’s the relationship between REST and CRUD?
    1. From [LogicMonitor](https://www.logicmonitor.com/blog/rest-vs-crud):
        1. REST and CRUD Work Together, but They Are Not the Same
            1. REST and CRUD work together because CRUD can exist within a REST environment, and their functions often correspond to each other, but they are not the same. The best way to differentiate between them is to remember that REST is a standard (an API architecture), and CRUD is a function. Understanding this essential but straightforward difference is necessary for understanding both.
        2. Because of the similarities between REST and CRUD, it’s easy to mistake them for having the same function. But that’s far from the truth. Delving a little bit deeper explores the differences between them.
            1. REST is an architectural system centered around resources and Hypermedia using HTTP commands. CRUD is a cycle meant to maintain records in a database setting. In its base form, CRUD is a way of manipulating information, describing the function of an application. REST is controlling data through HTTP commands. It is a way of creating, modifying, and deleting information for the user.
            2. CRUD functions can exist in a REST API, but REST APIs are not limited to CRUD functions. CRUD can operate within a REST architecture, but REST APIs can exist independent of CRUD. For example, a REST API can allow clients to reboot a server even if it doesn’t correspond to any CRUD functions. REST can do this as long as it uses the proper HTTP methods.
            3. REST usually refers to using data through HTTP commands. It’s a dogma to facilitate how users manipulate data onscreen and the information that’s being saved on the server. Programmers can create a REST API that can handle the essential CRUD functions, but the same can’t be said the other way around.
            4. The functions of REST and CRUD are similar (as discussed above), but they are not the same. PUT replaces a resource, even one that doesn’t exist yet. POST adds a new resource. Both of these commands create a new resource, but PUT is usually used to update resources that are already there. PATCH is mainly used to update a part of a resource, but PUT is used only to update an entire resource by replacing it.

2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?
    1. From [REST API Tutorial](https://restfulapi.net/rest-api-design-tutorial-with-example/):
        1. Identify the resources – Object Modeling. The first step in designing a REST API-based application is identifying the objects that will be presented as resources. ...
        2. Create Model URIs. ...
        3. Determine Resource Representations. ...
        4. Assigning HTTP Methods. ...
        5. More Actions.
