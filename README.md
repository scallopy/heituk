
# GR - Run it locally
A simple integration between Django API and React App

This project is made up of two main ones:

  - *growvick*: the Django project containing the REST API, along with all the
    back-end code;
  - *client*: the React project, with all Node dependencies, configs, and
    front-end related stuff.

    ## Run it locally

    In order to run the projects locally, you need to have Node, npm and Python
    installed on your machine.

    ### Running the Django project

    Just then you can clone the project from GitHub. So run:

    ```bash
    git clone git@github.com:scallopy/heituk-react.git
    ```

    Now, `cd` into the heituk-react/ folder:

    Make sure you have python3 installed in your machine:

    ```bash
    $ python --version
    Python 2.7.13

    $ which python3.5
    /usr/bin/python3.5

    $ alias python=/usr/bin/python3.5

    $ python --version
    Python 3.5.3

    ```

    First, let's create the python virtual environment to isolate our projects:

    ```bash
    python3 -m venv env
    ```

    Then, activate it:

    ```bash
    source env/bin/activate
    ```

    Add the needed Djano dependencies:

    ```bash
    pip install django djangorestframework django-cors-headers
    ```
    Now, cd into the django_react_proj/ folder and run migrations:

    ```bash

    $ python3 manage.py makemigrations

    $ python3 manage.py migrate

    ```

    Great, just need to run the project now:

    ```bash
    python manage.py runserver

    or

    python3 manage.py runserver
    ```

    That's it. Access the address http://localhost:8000/api/users/ and check
    for the API up and running.

    ### Running the React project

    First, `cd` the client/ directory and run:

    ```bash
    npm install
    ```

    Then, you just need to run the app via:

    ```bash
    npm start
    ```
# Integrating React App with Django in production

https://www.techiediaries.com/create-react-app-django/

https://fractalideas.com/blog/making-react-and-django-play-well-together/


#  create django-react-project

## Create backend:

###
https://docs.google.com/document/d/1o6QXta24f78ghKa9PUpsPxHQTL7ybDwuqrUTJxet8z0/edit#

$ python --version

Python 2.7.13

$ which python3.5
/usr/bin/python3.5

$ alias python='/usr/bin/python3.5'

$ python --version
Python 3.5.3

$ python3 -m venv venv

$ source venv/bin/activate

$ pip install django djangorestframework django-cors-headers

(env) scaly@debian:~/Dev/GR/django_react_proj$ django-admin --version

2.2.12


$ django-admin startproject django_react_proj

$ django-admin startapp growvick

- Create model User:

$ python3 manage.py makemigrations

$ python3 manage.py migrate

- Create data migration file:

It represents the direct manipulation of data into the database.

$ python3 manage.py makemigrations --empty --name users users

No installed app with label 'users'.

$ python3 manage.py makemigrations --empty --name growvick growvick

Migrations for 'growvick':

  growvick/migrations/0002_growvick.py

In short, the create_data method recovers the User model object and creates
initial data, just so that our database isn’t empty when the API starts.

The dependencies property relates the other files to be considered into the
migration process.

The operations are basically the actions Django has to perform once the
migration is triggered.

$ python3 manage.py migrate


## The REST API

  Create file serializers.py in growvick/

  Creat endpoints for users_list and users_detail

  Create views

  $ python manage.py runserver

  After you see the log showing our server is up and running, go to the browser

  and access http://localhost:8000/api/users/


## Building the React app

$ npm init react-app client

### - Create react-app:
https://github.com/facebook/create-react-app

$ cd client/

$ npm install bootstrap reactstrap axios --save

 SEE GR/django_react_proj/client/README.MD


