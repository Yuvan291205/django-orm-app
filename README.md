# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![er diiagram](https://github.com/Yuvan291205/django-orm-app/assets/138849170/a9994fef-a0e0-4b3f-8b9a-215cc566ddb5)


## DESIGN STEPS

### STEP 1: 
Create the folder'ex02' under directory 'unit2'

### STEP 2:
 clone the github respository into the directory "ex02" using the command "git clone" <url>

### STEP 3: 
Under the folder "django-orm-app" enter the directory titled "dataproject" and go to the "settings.py" under the file and " import in" line 34 set ALLOWED_HOST[*] and add myapp under the INSTALLED_APP

### STEP 4: 
Now return to the parent folder "dataproject" and install the application myapp using the command "python3 manage.pystartapp myapp"

### STEP 5:
Under the directory "myapp", open "models.py" and enter the code for the column headings

### STEP 6:
Under the directory "myapp",open "admin.py" and enter the code to set up the admin

### STEP 7:
Now return to the parent folder "dataproject", and into the prompt,enter the command "python3 manage.py make integrations"

### STEP 8:
Into the prompt, type the command "python3 manage.py migrate".

### STEP 9:
Now create a superuser by typing the command "python3 manage.py createsuperuser" into the prompt.Enter the username, leave the email address blank and enter the password to create to it

### STEP 10:
Into the prompt, type the command "python3 manage.py runserver 0:8000" to run the server at port number 8000

### STEP 11:
Now open the admin login page and enter the username and password to login.

### STEP 12:
Under the "MYAPP" section, click on "Add" next to the "Students" to create a record. Create 10 records in the same way.

### STEP 13:
Once the records are made, take a screenshot and save it.

### STEP 14:
Upload
Write your own steps

## PROGRAM
### model.py
```py
from django.db import models
from django.contrib import admin
# Create your models here.

class Student(models.Model):
    referencenumber=models.CharField(max_length=20,primary_key=True)
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    mobilenumber=models.IntegerField()
    mail=models.EmailField()
    number=models.IntegerField()
class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','mobilenumber','email','number')
```
### admin.py
```py
from django.contrib import admin
from .models import Student,StudentAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)
```


## OUTPUT
### Student List:
![Untitled](https://github.com/Yuvan291205/django-orm-app/assets/138849170/26bf8afa-8943-4c27-9b41-fc7af56d8d9e)
### Error List:
![Untitled](https://github.com/Yuvan291205/django-orm-app/assets/138849170/163f7961-72eb-4990-a668-01a85719274a)




## RESULT
The program is executed successfully
