# Django REST Framework & Docker

## Reading

### [Beginner’s Guide to Docker](https://wsvincent.com/beginners-guide-to-docker/)

- Linux containers
  - Docker is really just Linux containers which are a type of virtualization.
  - virtual machines are complete copies of a computer system from the operating system on up.
    - What’s the downside to a virtual machine? Size and speed.
  - Docker is a way to implement Linux containers

- Hello, World
  - A good command to inspect Docker is `docker info`
  - inspect the current image: `docker image ls`
  - inspect containers: `docker container ls -la`
    - `la` is needed with `ls` to show both stopped and running containers

- Images and Containers
  - An image is a snapshot in time of what a project contains.
  - A container is a running instance of the image.
  - Custom images are created using a `Dockerfile`
  - `docker-compose.yml` files are used to run the containers
  - There are a large number of official images available on Docker Hub for common software like different flavors of Linux, programming languages, and so on.

- Images
  - `Dockerfile` list of all the requirements needed to build an image.
  - Dockerfiles are read from top-to-bottom.
    - The first instruction must be the FROM command which lets us import a base image to use for our image.
    - This base image could be another Docker image or one we create entirely from scratch.

- Image Build
  - `docker image build .`

- Image Layers
  - Every image is made up of one or more layers.
  - The base layer is usually some flavor of Linux, e.g. alpine
  - Image layering:
    - each image layer is immutable–unchanged–like a git commit
    - Docker caches the steps in a Dockerfile to speed up subsequent builds
  - Order matters in a Dockerfile. Typically put code that won’t change often at the top, and code that will change at the end.

- Containers
  - The `docker-compose.yml` file is a list of container instructions.

### [Django for APIs - Library Website](https://djangoforapis.com/library-website-and-api/)

## Bookmark and Review

### [Beginner’s Guide to Django REST Framework](https://learndjango.com/tutorials/official-django-rest-framework-tutorial-beginners)

## Reading Questions

- What are the key components of a Docker container, and how do they help streamline the development and deployment of applications?

- Describe the primary steps involved in building a library website using Django, including essential components like models, views, and templates.

- Can you explain the primary differences between Django and Django REST framework?
