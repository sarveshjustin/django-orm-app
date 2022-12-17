# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

[entity](entity.png)

## DESIGN STEPS

STEP 1:

An Django application is created inside dataproject folder.

STEP 2:

A python program is written to create a table to store and retrieve data.

STEP 3:

The table is created with 6 fields in which the username field is made as PrimaryKey.

STEP 4:

Then the project files migrated. A superuser is also created.

STEP 5:

Now the server side program is executed .

STEP 6:

The admin page of our website is accessed using username and password.

STEP 7:

Records are added and saved in the table inside the database.
Write your own steps

## PROGRAM

```
from django.db import models
from django.contrib import admin

class deliverydatabase(models.Model):
    username_primary_key = models.CharField(max_length=30, help_text="User id must be unique", primary_key=True,unique=True)
    address= models.CharField(max_length=30)
    phone_number = models.IntegerField()
    order_name = models.CharField(max_length=20)
    coupon_code = models.CharField(max_length=20)
    email = models.EmailField(max_length=50,unique=True)

class deliveryadmin(admin.ModelAdmin):
    list_display = ('username_primary_key', 'address', 'phone_number', 'order_name','coupon_code','email')

```

## OUTPUT

[output](output.png)

## RESULT
Thus a Django application is successfully developed to store and retrieve data from a database using Object Relational Mapping(ORM).