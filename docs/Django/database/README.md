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

## Create Models for database
```python
from django.db import models

class Topic(models.Model):
    topic_name = models.CharField(max_length=264, unique=True)

    def __str__(self):
        return self.topic_name


class Webpage(models.Model):
    topic = models.ForeignKey(Topic, on_delete=models.CASCADE)
    name = models.CharField(max_length=264, unique=True)
    url = models.URLField(unique=True)

    def __str__(self):
        return self.name


class AccessRecord(models.Model):
    name = models.ForeignKey(Webpage, on_delete=models.CASCADE)
    date = models.DateField()

    def __str__(self):
        return str(self.date)
        
```

and then run
```
python migrate.py migrate
python migrate.py makemigrations <app_name>
python migrate.py migrate
```
and it will create a table (models) from the following attributes on class.

Then, you can add a new data using GUI or command lines.
