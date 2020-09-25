# Read:31 Summary
## Docker
* `Docker` : which is a way to isolate and run entire applications. With Docker it doesn’t matter if you are using a
Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more.
* With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can 
be shared among team members so everyone is working on the same setup. Wins all around.
* Docker is really just Linux containers which are a type of virtualization.
* Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers
use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.
* in recent years Linux containers, also known as “containerization,” has become increasingly popular. For most applications, a virtual machine provides far more resources
than are needed and a container is more than sufficient.

***This, fundamentally, is what Docker is. A way to implement Linux containers!***

* An analogy we can use here is that of homes and apartments. Virtual Machines are like homes: stand-alone buildings with their own infrastructure including 
plumbing and heating, as well as a kitchen, bathrooms, bedrooms, and so on. Docker containers are like apartments: they share common infrastructure like plumbing 
and heating, but come in various sizes that match the exact needs of an owner.

### Containers vs Virtual Environments
* Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and 
Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.
* But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper
version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.
* Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
## install docker 
* download the desktop app on our computer and create a free account
* if you are on Linux, you will need to add `Docker Compose` manually. You can do this by running the command `sudo pip install docker-compose`
after your Docker installation is complete.
* to confirm Docker installed correctly we can run our first command `docker run hello-world`. This will download an official image and then run the container.
* you can run an Ubuntu container with:` docker run -it ubuntu bash`
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Images and Containers
* Images and containers are the two fundamental concepts to grasp when you start with Docker. An `image` is a snapshot in time of what a project contains. A `container` 
is a running instance of the image.
* A baking analogy we can use here is as follows:

  * A Dockerfile is the recipe for a cake
  * An image is a snapshot of the recipe at a given time
  * A docker-compose.yml says how to make the cake
  * And the container is the actual, baked cake
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Conclusion
* Docker is a way to run Linux containers
* Containers are a lightweight alternative to Virtual Machines
* `Dockerfile` is a list of instructions for creating an image
* Images are made up of one or more layers
* Containers are a running instance of an image
* `docker-compose.yml` controls how to run the container
* Containers are stateless and ephemeral in nature. We can link the local filesystem via `volumes` but things become more complex with databases 

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Library Website and API
* Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; 
it always must be added to a project after Django itself has been installed and configured.
* The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a 
collection of URL endpoints containing available HTTP verbs that return JSON.
* To illustrate these concepts, we will build out a basic Library website with traditional Django and then extend it into a web API with Django REST Framework.

* The files have the following roles:
```
__init__.py is a Python way to treat a directory as a package; it is empty
asgi.py stands for Asynchronous Server Gateway Interface and is a new option in Django 3.0+
settings.py contains all the configuration for our project
urls.py controls the top-level URL routes
wsgi.py stands for Web Server Gateway Interface and helps Django serve the eventual web pages
manage.py executes various Django commands such as running the local web server or creating a new app.
admin.py is a configuration file for the built-in Django Admin app
apps.py is a configuration file for the app itself
the migrations/ directory stores migrations files for database changes
models.py is where we define our database models
tests.py is for our app-specific tests
views.py is where we handle the request/response logic for our web app
```
* A `serializer` : translates data into a format that is easy to consume over the internet, typically JSON, and is displayed at an API endpoint





























