# Read:28 Summary
## Django Forms
* An `HTML Form` : is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server.
* `Forms` : are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes,
radio buttons, date pickers and so on. Forms are also a relatively secure way of sharing data with the server, as they allow us to send data in POST requests
with cross-site request forgery protection.
* `Django Forms` : take a lot of the work by providing a framework that lets you define forms and their fields programmatically, and then use
these objects to both generate the form HTML code and handle much of the validation and user interaction.
*  form may have any number of other input elements and their associated labels. The field's type attribute defines what sort of widget will be displayed.
The name and id of the field are used to identify the field in JavaScript/CSS/HTML, while value defines the initial value for the field when it is first 
displayed. The matching team label is specified using the label tag (see "Enter name" above), with a for field containing the id value of the associated input.
* The submit input will be displayed as a button (by default) that can be pressed by the user to upload the data in all the other input elements in the form
to the server (in this case, just the team_name). The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):
  * `action` : The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be 
  submitted back to the current page URL.
  * `method` : The HTTP method used to send the data: post or get.
    * The `POST` method should always be used if the data is going to result in a change to the server's database because this can be made more resistant to 
    cross-site forgery request attacks.
    * The `GET` method should only be used for forms that don't change user data (e.g. a search form). It is recommended for when you want to be able
    to bookmark or share the URL.
* creating the HTML, validating the returned data, re-displaying the entered data with error reports if needed, and performing the desired operation 
on valid data can all take quite a lot of effort to "get right". Django makes this a lot easier, by taking away some of the heavy lifting and repetitive code!
* the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into 
which we pass a context containing the data to be displayed). What makes things more complicated is that the server also needs to be able to process 
data provided by the user, and redisplay the page if there are any errors.
* the main things that Django's form handling does are:
  * Display the default form the first time it is requested by the user.

  * Receive data from a submit request and bind it to the form.

  * Clean and validate the data.

  * If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.

  * If all data is valid, perform required actions (e.g. save the data, send an email, return the result of a search, upload a file, etc.)

  * Once all actions are complete, redirect the user to another page.

* The `Form class` : is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values,
valid values, and (once validated) the error messages associated with invalid fields. The class also provides methods for rendering itself in templates 
using predefined formats (tables, lists, etc.) or for getting the value of any element (enabling fine-grained manual rendering).
* `ModelForm` : helper class to create the form from your model. This ModelForm can then be used within your views in exactly the same way as an ordinary Form.
* Creating and handling forms can be a complicated process! Django makes it much easier by providing programmatic mechanisms to declare, render, and validate 
forms. Furthermore, Django provides generic form editing views that can do almost all the work to define pages that can create, edit, and delete 
records associated with a single model instance.

    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
