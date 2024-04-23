## Starting a Django project
https://www.youtube.com/watch?v=fsVY66QBhwM&t=363s
* Make a directory and cd into it. 
* Creating a virtual environment:
		python3 -m venv .venv
* Activating a virtual environment: 
		. .venv/bin/activate
* pip install django 
* django-admin startproject djangouploads .
* python3 manage.py runserver
* python3 manage.py migrate

* python3 manage.py makemigrations djangouploads 

* python3 manage.py createsuperuser
### models.py
from django.db import models 

class Movie(models.Model):
	name = models.CharField(max_length = 200)
	image = models.ImageField(upload_to = 'files/covers')
### admin.py
from django.contrib import admin
from .models import Movie

admin.site.register(Movie)

### settings.py 
INSTALLED_APPS me add your newly created app. 