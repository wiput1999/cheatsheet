## Start the project
Get into the project

- `__init.py__` makes the Python to treat the folder as package. It will be a blank file.
- `settings.py` Store Settings
- `urls.py` store URL (page) for the file
- `wsgi.py` acts as Web Server Gateway Interface, as it will help to deploy Django to production
- `manage.py` associates with commands

## Run the project
Using manage.py to run
```
python manage.py runserver
```
or click run on PyCharm

> Web App != Project

## Create new Web Applications
```
python manage.py startapp <app_name>
```

and it will create a new folder with `<app_name>`
- `__init__` make Python treats it as package
- `admin.py` register models to benefits admin interface
- `apps.py` place application's configurations
- `models.py` store data models + store entity/relationships of data
- `tests.py` store functions to test code
- `views.py` handle request + response
- "migrations" folder store database informations on models + templates

