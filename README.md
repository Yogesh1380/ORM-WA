# Ex02 Django ORM Web Application
## Date: 08.03.2025

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
admin.py
~~~
from django.contrib import admin
from .models import book,bookadmin
admin.site.register(book,bookadmin)
~~~
models.py
~~~
from django.db import models
from django.contrib import admin
class book(models.Model):
    Book_name=models.CharField(max_length=100)
    Author=models.CharField(max_length=100)
    Co_author=models.CharField(max_length=100)
    Book_code=models.IntegerField()
    Publisher=models.CharField(max_length=100)
    MRP=models.IntegerField()
class bookadmin(admin.ModelAdmin):
    list_display=("Book_name","Author","Co_author","Book_code","Publisher","MRP")
~~~
urls.pr
~~~
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]

~~~
## OUTPUT
![orm 1image](https://github.com/user-attachments/assets/0daf338e-0e27-4716-825f-40b8320e050f)

![orm 2image](https://github.com/user-attachments/assets/a284592d-0d4d-4eb2-b71e-2e3032f80d34)

![orm 3image](https://github.com/user-attachments/assets/aed26a58-a286-4076-b603-043d08fa7f88)
## RESULT
Thus the program for creating movies database using ORM hass been executed successfully.
