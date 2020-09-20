# Read:27 Summary
## Django Models
* Django web applications access and manage data through Python objects referred to as models. 
* `Models`: define the structure of stored data, including the field types and possibly also 
their maximum size, default values, selection list options, help text for documentation, label text for forms, etc. 
* The definition of the model is independent of the underlying database — you can choose one of several as part of your project settings. Once you've chosen 
what database you want to use, you don't need to talk to it directly at all — you just write your model structure and other code, and Django handles all the
dirty work of communicating with the database for you
### what data we need to store and the relationships between the different objects ??
* When designing your models it makes sense to have separate models for every "object" (a group of related information)
* Once we've decided on our models and field, we need to think about the relationships. Django allows you to define 
relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).
* he multiplicities are the numbers on the diagram showing the numbers (maximum and minimum) of each model that may be present in the relationship
* `Models`: are usually defined in an application's models.py file. They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata.
### features inside the model:
  * `Fields` : A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables.
  Each database record (row) will consist of one of each field value
  * `metadata` : is to control the default ordering of records returned when you query the model type. You do this by specifying the match order in a list
  of field names to the ordering attribute
  * `Methods` : Minimally, in every model you should define the standard Python class method __str__() to return a human-readable string for each object. This string is used 
  to represent individual records in the administration site (and anywhere else you need to refer to a model instance). Often this will return a title or name field 
  from the model.

* In this section we will start defining the models for the library. Open models.py (in /locallibrary/catalog/). The boilerplate at the top of the page imports the models
module, which contains the model base class models.Model that our models will inherit from.`from django.db import models`
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Django Admin
* The `Django admin` application : can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you
a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data. 
* The admin application can also be useful for managing data in production, depending on the type of website. The Django project recommends it only for internal
data management (i.e. just for use by admins, or people internal to your organization), as the model-centric approach is not necessarily the best possible 
interface for all users, and exposes a lot of unnecessary detail about the models. 
* All the configuration required to include the admin application in your website was done automatically when you created the skeleton project 
* First, open admin.py in the catalog application, then do `from django.contrib import admin`
* Register the models by copying the following text into the bottom of the file. This code simply imports the models and then calls `admin.site.register`
to register each of them.
* In order to view and create records we also need this user to have permissions to manage all our objects.  You can create a `"superuser"` account that has
full access to the site and all needed permissions using manage.py.
* Call the following command : `python3 manage.py createsuperuser`, in the same directory as manage.py, to create the superuser. You will be prompted 
to enter a username, email address, and strong password.
* To login to the site, open the /admin URL (e.g. http://127.0.0.1:8000/admin) and enter your new superuser userid and password credentials
(you'll be redirected to the login page, and then back to the /admin URL after you've entered your details).
* Django does a pretty good job of creating a basic admin site using the information from the registered models:
  * Each model has a list of individual records, identified by the string created with the model's __str__() method, and linked to detail views/forms 
  for editing. By default, this view has an action menu at the top that you can use to perform bulk delete operations on records.
  * The model detail record forms for editing and adding records contain all the fields in the model, laid out vertically in their declaration order.  
----------------------------------------------------------------------------------------------------------------------------------------------------------------------





























