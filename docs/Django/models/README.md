# Models
Models is similarly to database. Python will generate some `sqllite` file to locally use in the PC, so SQL database is not quite a requirement from now. 

## Models Setup
Normally, Django will use SQLLite as a database and it is already built into the Python.

## Generating simple model
โดยตัว model ก็จะเหมือนๆกับ ตาราง SQL Table 

ก่อนที่จะทำ Model ก็ต้องให้มันสร้าง Table ของมันเองก่อน (default model) โดยการใช้คำสั่ง

```
python manage.py migrate
```

และก็เข้าไปทำการ register ตัว app เพื่อให้ร่่วมใช้งาน model ได้ด้วย
```
python manage.py makemigrations <app_name>
```

แล้วก็ไป `python manage.py migrate` อีกรอบเพื่อให้แน่ใจว่าทำงานได้ถูกต้องแล้ว

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
