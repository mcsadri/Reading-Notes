# Serverless Functions

## Reading

### [What is Serverless Computing? (through the `Pros and Cons` section)](https://www.ibm.com/cloud/learn/serverless)

- Serverless is a cloud computing application development and execution model that enables developers to build and run application code without provisioning or managing servers or backend infrastructure.

### Additional Resources

- [venv - Creation of Virtual Environments](https://docs.python.org/3/library/venv.html)
- [Vercel - Get Started](https://vercel.com/docs/get-started)
- [http.server](https://pymotw.com/3/http.server/index.html)
- [Requests](https://requests.readthedocs.io/en/latest/)
- [Python & APIs](https://realpython.com/python-api/)

## Videos

- doodah

### [What is Serverless?](https://www.youtube.com/watch?v=vxJobGtqKVM)

## Even More Resources

- [Serverless Functions](https://vercel.com/docs/concepts/functions/serverless-functions)
- [Effective Python Environment](https://realpython.com/effective-python-environment/)

---

## Reading Questions

- What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?
  - devs do deploy to cloud containers, instead of to specific servers
  - cloud provider manages and maintains all infrastructure
  - scalable, elastic services
  - only billed for executuion time

- How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?
  - Deploy
  - Configure
  - Assign a Domain
  - Make Changes
  - Collaborate
  - Add Compute
  - Monitor

- What are APIs, and how can they be utilized in Python applications to access and manipulate data from external sources?
  - an API acts as a communication layer that allows different systems to talk to each other without having to understand exactly what each other does
  - make a request for information or data, and the API returns a response with what you requested
  - SOAP vs REST vs GraphQL
    - SOAP (Simple Object Access Protocol) is typically associated with the enterprise world, has a stricter contract-based usage, and is mostly designed around actions.
    - REST (Representational State Transfer) is typically used for public APIs and is ideal for fetching data from the web. It’s much lighter and closer to the HTTP specification than SOAP.
    - GraphQL is a very flexible query language for APIs, where the clients decide exactly what they want to fetch from the server instead of the server deciding what to send

- What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?
  - a simple HTTP library
  - Requests allows you to send HTTP/1.1 requests extremely easily. There’s no need to manually add query strings to your URLs, or to form-encode your POST data. Keep-alive and HTTP connection pooling are 100% automatic
  - `>>> r = requests.post('https://httpbin.org/post', data={'key': 'value'})`
