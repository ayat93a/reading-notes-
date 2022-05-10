# Getting started with Django 
*steps to start new project*
`pip install pipenv`
`pipenv install django`
`pipenv shell` or `pipenv run` to start the project
`django-admin startproject *project name*`
`django-admin startapp *app name*`

# How Django Works Behind the Scenes
Django is a Python-based web framework that is utilized by millions of developers and billions of users via apps like Instagram. It is open source, which means that the code may be downloaded for free from Github and used alongside the official documentation by any developer.

# Django is opinionated
Opinionated frames are ones that have strong feelings about the "correct" approach to complete a task. Because the right way to implement something is usually well-understood and well-documented, they frequently support rapid development in a specific domain (fixing problems of a specific sort). However, they can be less adaptable when handling challenges outside of their primary domain, with fewer options for components and methodologies.

# What does Django code look like?
In a traditional data-driven website, a web application waits for HTTP requests from the web browser (or other client). When a request is received the application works out what is needed based on the URL and possibly information in POST data or GET data. Depending on what is required it may then read or write information from a database or perform other tasks required to satisfy the request. The application will then return a response to the web browser, often dynamically creating an HTML page for the browser to display by inserting the retrieved data into placeholders in an HTML template.\
Django web applications typically group the code that handles each of these steps into separate files:
![](./basic-django.png)
