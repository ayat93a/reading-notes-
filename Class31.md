# Django REST Framework & Docker
# Django REST Framework:
REST (Representational state transfer) is a conventional architecture for building and communicating with web services. They use HTTP request methods to make it easier for the request-response cycle and typically transfer data using JSON format.\
An API (Application Programming Interface), as the name suggests, is an interface that defines different interactions between different software components. Rest APIs are created using Django Rest Framework. It is a toolset that is assembled on top of the Django web framework, reducing the amount of code you need to write to create REST interfaces.

# Introduction to Docker:
To materialize a Django project, frequently you require an off-the-rack solution in form of a library or dependency.
This is not an issue because is often registered in the requirements.txt file, which is a file that lists all the modules that are needed for the Django project to work.\
The conflict starts when you attempt to share the entire project with another individual who wants to run and test it because, unfortunately, the user will have to perform the setup from scratch every time you make notable changes in the libraries and dependencies.
This is where containerization and docker fall in. Docker is an incredibly popular containerization platform that solves the library and dependency issue once and for all.