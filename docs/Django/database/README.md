# Database Setup
Normally, Django will use SQLLite as a database and it is already built into the Python.

## Generating simple model
Model = SQL table

So, Django needs to create a model for users + itself.<br>
To generate, use

```
python manage.py migrate
```

and then register changes to app.<br>
To register, use
```
python manage.py makemigrations <app_name>
```

and do the migration again, then we can play with models.

## Database Binding
You might want to use PostgreSQL instead for further usage. 

- Install database binding
- Change keys in DATABASE default

by changing in `settings.py` in the project folder.
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}
```