#CA1

This is a simple web application built with Django that allows users to perform CRUD (Create, Read, Update, Delete) operations on a database of drivers and cars.

Developing process :

- Define the requirements: Start by defining the requirements for the application. This involves determining the features and functionality needed, such as creating, reading, updating, and deleting records for both cars and drivers, and creating a user interface to display and interact with the data.

- Create the Django project: Create a new Django project using the django-admin startproject command. This will create a new project directory and some initial files.

- Set up the database: Set up the database configuration in the settings.py file and create the necessary models for cars and drivers.

- Create views and templates: Create views to handle requests from the user interface, and templates to display the data in a user-friendly way. These views will include functions to perform CRUD operations on the database.

- Define URLs: Define URLs for the different views so that users can navigate to the appropriate pages.

Purpose :

The purpose of the application would be to help manage and organize data related to F1 cars and drivers, making it easier for users to access and manipulate this information as needed. Allowing users to perform basic CRUD (Create, Read, Update, Delete)


Models : 

class Driver(models.Model):  
        number = models.IntegerField();  
        first_name = models.CharField(max_length=200)  
        last_name = models.CharField(max_length=200)  
        age = models.IntegerField()  
    
class Car(models.Model):
        team = models.CharField(max_length=200)  
        colour = models.CharField(max_length=200)  
        driver = models.ForeignKey(Driver, on_delete=models.CASCADE)  
        horses = models.IntegerField()  
        aero = models.IntegerField()  
        safety = models.IntegerField()  
