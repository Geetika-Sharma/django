# Django
Django is a high-level web framework for Python that enables rapid development of secure and maintainable web applications. It follows the Model-View-Template (MVT) architectural pattern, which is similar to the Model-View-Controller (MVC) pattern but with some differences in terminology and structure.

## Table of Contents
- [Key Features](#key-features)
- [Directory Structure generated with `startproject`](#directory-structure-generated-with-startproject)
- [Directory Structure generated with `startapp`](#directory-structure-generated-with-startapp)
- [ORM](#orm)
## Key Features
Key features of Django:

1. **Admin Interface:** Django provides an automatic admin interface for managing application data. The admin interface is customizable and allows developers to handle CRUD operations on the database without writing custom code.

2. **ORM (Object-Relational Mapping):** Django's ORM allows you to interact with the database using Python classes and objects, making it easier to work with databases without writing raw SQL queries.

3. **URL Routing:** Django has a powerful URL routing system that allows you to define URL patterns and map them to specific views (controller in MVC/MVT).

4. **Template Engine:** Django comes with a template engine that allows you to separate HTML code from Python code, making it easier to design the frontend of your application.

5. **Forms Handling:** Django provides form handling capabilities, making it simple to create and validate forms on the server side.

6. **Authentication and Authorization:** Django has built-in support for user authentication and authorization, allowing you to manage user accounts, permissions, and sessions easily.

7. **Security Features:** Django includes various security features, such as protection against common web vulnerabilities like SQL injection, cross-site scripting (XSS), and cross-site request forgery (CSRF).

8. **Middleware:** Django allows you to define middleware components to process requests and responses globally across your application.

9. **Internationalization and Localization:** Django supports multiple languages and time zones, making it easy to build applications that are accessible to users from different regions.

10. **Scalability:** Django is designed to handle projects of all sizes, from small applications to large-scale, high-traffic websites.

Django encourages the "Don't Repeat Yourself" (DRY) principle and follows best practices, making it suitable for building maintainable and reusable code. It is widely used in the web development community and has a rich ecosystem of packages and extensions to extend its functionality.

To get started with Django, you'll need to install it first. You can do this using pip:

```bash
pip install Django
```

Once installed, you can create a new Django project using the following command:

```bash
django-admin startproject projectname
```

Replace "projectname" with the name of your project. Then, navigate to the project directory and create a Django app using:

```bash
python manage.py startapp appname
```

Replace "appname" with the name of your app. With the app created, you can define models, views, templates, and URL patterns to build your web application.

Django provides comprehensive documentation, tutorials, and a friendly community to help you get started and explore its features in more detail.

## Directory Structure generated with `startproject`
When you create a new Django project using the `django-admin startproject demo` command, it generates a directory structure with several files and folders. Each of these files serves a specific purpose and plays an essential role in the Django project. Here's a detailed explanation of the key files created:

1. **`manage.py`:**
   - The `manage.py` script is a command-line utility that provides various tools for managing the Django project. It is used to run development servers, create database tables, run tests, and perform other administrative tasks.
   - Common commands include:
     - `python manage.py runserver`: Starts the development server.
     - `python manage.py migrate`: Synchronizes the database schema with the models.
     - `python manage.py createsuperuser`: Creates a superuser for the admin interface.

2. **`demo/` (Directory):**
   - The `demo` directory contains the Django project's main settings and configuration. It is the top-level package that houses the entire project.

3. **`demo/settings.py`:**
   - `settings.py` is one of the most crucial files in a Django project. It contains all the project settings, such as database configuration, installed apps, middleware, static and media file settings, internationalization settings, and more.
   - This file defines Django settings for different environments (e.g., development, production) using the concept of multiple settings files.

4. **`demo/urls.py`:**
   - `urls.py` is the URL configuration for the project. It contains URL patterns and their corresponding views (controllers) that handle different web requests.
   - The `urlpatterns` variable is a list of URL patterns associated with specific views.

5. **`demo/asgi.py` and `demo/wsgi.py`:**
   - `asgi.py` and `wsgi.py` are used for ASGI (Asynchronous Server Gateway Interface) and WSGI (Web Server Gateway Interface), respectively.
   - These files are used when deploying the Django project with different servers or interfaces.

6. **`demo/__init__.py`:**
   - The `__init__.py` file makes the `demo` directory a Python package. It may be empty or contain initialization code.

7. **`manage.py`:**
   - We discussed this file earlier. It's located in the top-level directory and is used to execute various management commands.

8. **`db.sqlite3`:**
   - This is the default SQLite database file that Django creates when you first run migrations. In more complex projects, you might use other databases like PostgreSQL, MySQL, etc., but for the initial setup, Django uses SQLite.

After running `django-admin startproject demo`, the project structure will look like this:

```
demo/
|-- demo/
|   |-- asgi.py
|   |-- __init__.py
|   |-- settings.py
|   |-- urls.py
|   |-- wsgi.py
|-- manage.py
|-- db.sqlite3
```

The outer `demo` directory contains the main project settings and the `manage.py` file, while the inner `demo` directory is the Python package that houses the project-specific files like settings and URL configurations.

As you build your Django project, you'll create additional files and directories for your Django apps, static files, templates, and media files. The project directory structure will grow and become more organized as you add more components to your application.

## Directory Structure generated with `startapp`
When you create a new Django app using the `python3 manage.py startapp myapp` command, Django generates a directory structure with several files and folders. Each of these files serves a specific purpose and plays an essential role in the Django app. Here's a detailed explanation of the key files created:

```
myapp/
|-- migrations/
|   |-- __init__.py
|-- __init__.py
|-- admin.py
|-- apps.py
|-- models.py
|-- tests.py
|-- views.py
```

1. **`migrations/`:**
   - The `migrations` directory is automatically created to manage database schema changes for your app. Whenever you make changes to your models (adding, modifying, or deleting), Django will create migration files in this directory to reflect those changes in the database schema.

2. **`__init__.py`:**
   - The `__init__.py` file makes the `myapp` directory a Python package. It may be empty or contain initialization code.

3. **`admin.py`:**
   - The `admin.py` file is used to register your app's models with the Django admin interface. By registering models, you can manage them using the admin site.

4. **`apps.py`:**
   - The `apps.py` file contains the app's configuration. You can modify this file to customize the behavior of your app, although it's generally not used frequently.

5. **`models.py`:**
   - The `models.py` file is where you define the data models (database tables) for your app. You'll use Django's model classes to specify the structure of the database tables and their relationships.

6. **`tests.py`:**
   - The `tests.py` file is where you can write test cases for your app. Django encourages writing tests to ensure the correctness of your application.

7. **`views.py`:**
   - The `views.py` file is where you define the views (controllers) for your app. Views handle incoming requests, process data, and render templates to produce the HTTP responses.

As you develop your Django app, you may create additional directories and files for templates, static files, and other resources specific to your app. The structure will grow and become more complex as you add more functionality to your app.

After running `python3 manage.py startapp myapp`, the app directory structure will look like the one described above. The `migrations` directory will initially be empty, but Django will populate it with migration files as you make changes to your app's models and run the `python3 manage.py makemigrations` command.

### ORM
ORM stands for Object-Relational Mapping. It is a technique that allows you to interact with your database using Python classes and objects, without having to write raw SQL queries. Django's ORM is powerful, efficient, and easy to use, making database operations more intuitive and abstracted from low-level database interactions.

Key concepts and features of Django ORM:

1. **Models:** In Django, a model is a Python class that represents a database table. Each attribute of the class corresponds to a database field, and instances of the class represent individual rows in the table. Models are defined in the `models.py` file of your Django app.

2. **Model Fields:** Django provides various field types to define the attributes of a model. Some common field types include `CharField`, `IntegerField`, `DateField`, `ForeignKey`, `ManyToManyField`, etc. These field types define the data type and constraints for the corresponding database fields.

3. **Model Manager:** Each Django model has a default manager, which is responsible for querying the database and performing database operations. The manager provides methods like `all()`, `filter()`, `get()`, `create()`, etc., to perform common database queries.

4. **QuerySets:** A QuerySet is a collection of database queries that can be executed to retrieve data from the database. It allows you to chain multiple query operations and perform complex lookups. QuerySets are lazy, which means they are not executed until you actually need the data.

5. **Migrations:** Migrations are Django's way of managing changes to your database schema over time. When you make changes to your models, such as adding or modifying fields, Django creates migration files that apply these changes to the database in a consistent and automated way.

6. **Database API:** Django's ORM provides a database-agnostic API, allowing you to switch databases (e.g., SQLite, PostgreSQL, MySQL) without changing your code. Django abstracts the differences between databases, making it easy to work with different database backends.

Example of a simple Django model:

```python
# models.py

from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.CharField(max_length=100)
    publication_date = models.DateField()

    def __str__(self):
        return self.title
```

With this model defined, you can perform various database operations, such as creating, updating, querying, and deleting records, using Python code. For example:

```python
# Creating a new book instance and saving it to the database
book = Book(title="Sample Book", author="John Doe", publication_date="2023-07-29")
book.save()

# Querying books with a certain condition
recent_books = Book.objects.filter(publication_date__gte="2022-01-01")

# Updating a book's title
book = Book.objects.get(id=1)
book.title = "New Title"
book.save()

# Deleting a book
book = Book.objects.get(id=2)
book.delete()
```