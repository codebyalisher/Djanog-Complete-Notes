# Djanog-Complete-Notes

**Django Complete Notes**

Daily routine base activities on websites and their data is stored on server in database using any programming language.

**Django:** It is a python framework that is used to build the large scale applications.

For example: a company that has a little lemon static website and now they want to build its next version using Django framework. We will do this by using our existing knowledge, explore Django, build prototype, present this proto to the administrative team.

**Django Course Topics: contains following topics.**

1-Introduction to Django,

2- Views

3- Models

4-Template

**1-Introduction to Django:**

For the development of the web Developer has two options either build everything from scratch or use the build in known as framework/toolkit(it consists of all the components needed for the application like login,models). Django is an open source web development framework with richness of python .it famous when news paper website was created by it.It is used when require high volume of Text content,Media Files and Heavy Traffic. Its use is bcz of its robustness ,scalability,security and ,supportive community and detailed documentation, convenience. It provides,libraies,apis and templates which are easily scalable. It is useful for choosing the ecommerce,health,finance and transport, travel and social media.

**Differentiate between components app,and project structure:**

**Dynamic website require following(Internet Protocol, web server configuration, data retrievel and storage).**

**Project Structure; represents the entire web application ,Django provides the set of commands which provides the structure of the project that contains the settings and configuration for the entire application**.

**App:** it is the submodule of the project which is for specific purpose,it contains,many apps and can be used many times without crating again and again. This is add by the command as; python manage.py startapp appname which provides the sperate directory for it inside the project structure. Project must recognized the app so it is added in the installed app option in setting.py file.

**A Django app** is set of code that connects with the the various parts of the framework. There are few places where Django is need to interact with the installed apps. This is mainly for configuration.

Learn to use the basic commands to build the Django project with Django-admin and manage.py

Create the virtual environment. Install the Django .now create the project Django-admin startproject projectname.

**Python manage.py:** is a command line utility that works as a admin Django command. You can change the Django command line with manage.py file as it is used in the settings.py **. To work on the project developers have two options for commands** Django-admin and manag.py to perform administrative tasks . any can be used but there is a little diference.

**Django-admin** has a feature that it provdes the ready to use the admin interface in the form of command line utility as Django-admin.it is the command line utility for the djagno-admin for administrative tasks. It is present In the script folder in the installed Django environment directory and this Django-admin utility is executed from the inside of the terminal. It is automatically installed when Django is installed and it should on the system path. . It sets the Django settings module environment variable so that it points to your project setings.py file

**Manage.py script :** it is the local version of Django-admin and located inside the project folder. It sets the Django settings module environment variable so that it points to your project setings.py file . it is created automatically everytime when project is created. It is specific to the virtual environment. When to work on the single project usually maange.py is used to perform the Django-admin tasks but however you need to switch the multiple settings file use the Django-admin command with Django_settings_module option. Using the dango-admin command to create the project it creates the setting and maange.py file again and again inside the directory

**Create an app inside existing project:** pyhton manage.py startapp appname

**3-Tier Architechure:**

![image](https://github.com/codebyalisher/Djanog-Complete-Notes/assets/62823194/267ba2f9-a0ff-49fe-9bb8-95b5db81c3a1)


**Show the MVT pattern with code reusability:**

![image](https://github.com/codebyalisher/Djanog-Complete-Notes/assets/62823194/4ad48519-3858-4cf8-9a77-0161ad7f6cb7)


**2-Views: It is used to create the logic to handle the data on server**

Process http request, request/response and http

http methods, url mapping and error handling,class based views.

**URL configuration:** to create the ush at app level- and pass it to the project level url file.

**Routing**: To map the view to URL is called routing. HTTP-E Send's the web resources like HTML webpages.

**HTTP Methods:** Get, post, put, delete,

Get: /imagespath,

**Headers:** contains additional information like server name, Server Port, Require method and content Type and content body.

**HTTP Responses:** Server name , Time, HTP Version, status code.

**Status code**: 100-199informational, 200- 298 Successful,302 It shows the temporary moved resource. When server receives response, it automatically submitt resource at new path.

301 Permanent moved resource.

**Clint error:** indicates the bad request or content or Can't processed by the Server.

**Server error responses:** indicates that error occur on Server during process request.

**HTT/HTTPS:** The difference between is that encryption which only computer change and read. It is protocol used by Server and client to transfer web resources. Request is made in browser by client and resources are sent back by server.

**→ HTTP Req:** has method, path, version, Headers.

**→ HTTP Response:** contains status code and other additional info. Request – response cycle is done between web browser and server. It is begin in Django by URL in browser, once URL is found in

URL.py file in the project, then it finds the views associated to it and then it receives the request as object and then defines the appropriate HTTP method and sent the back as HTTP Response.

**=) Creating Request and  Responses objects:** we can do this by assigning the request object properties/attributes to a variable and then These variables can be used in the String and then this string will be sent as response.je.

def home(req):

name=req.name.

path = req.path

method = req method

Str = f " \<br\>

\<br\>path: { path }

\<br\> method: {methad} "".

return HTTP Response (str). This was for Request.

**→ Similarly**: for Response i.e. res = Rsponse()

res. Headers('age']=20. and then pass to string as \<br\>age: {res. Heaters}

Developer use these requested response when they are working with methods.

**=) understanding URLS:**  when browser is open ad something is searched, it is basically address is called URL (Uniform resource Locator) and it points/shows the web source on server and it can be made by – many routes/urls. It contains the following http: www: Sub-domain/filepath, http sends the plain text and HTTPS: sends the scheme and encrypts the data.

**Top level-domain:** country/category and **Second -level-domain :** is for organization, individual .

**Parmeter:** it is the value. Structure additional information inside URL to catch any part of URL to catch values from file-path query String: it is used to find the specific values on the base of query string and parameter. i.e. <https://.com/file?year=2023>, -query string can be passed as many using parameters.

**=) Mapping URLS with parameters:** url is mapped with view function.

Sometime developers pass information to view function for additional processing.

in django, developor has option to pass values as URLs parameter by using url as source of information. Here we will use URL parameters to retrieve data from URL and send data to the view function for processing. Also we will use angular brackets/path converter to captcher the values from URL.

j.e- https-domain-name/drink/espresso it’s the value as a parameter and can be passed to the view function from CURL Converter . We can capture this value from url using angular brackets/type-converter inside the "URLpattern = ['path("/\<str:name\>)", views) here name variable is used to capture the value and then this is passed as an argument to the view function with request object. Overall url parameters mapped to view function for searching criteria, forms, data models, data structure.

**Regular Expressions:** similar to path converter, Regexp are also used in URL j.e. url-partem (re-path('menu-item/((0-9) (2)/8, views. function), They are set of characters that specify a pattern and are used to search or find pattern in string. In diango, developers use Regexp to define and extract and validate dynamic URL paths before send to associated view function.

**→we define paths using Regular-path and Regexp-path i.e. Urlpattern=[ ( path ('1', view),re-path(r’\^menu-item/([0-9]{2}/\$,view)],here 0-9 shows the grouping of regexp and 2 shows the preceding characters.**

**⇒Enor Handling:** To handle the client and server response error, the view's file for these errors should be defined in the project level. for This, we will use the custom view classes HTTPNotford-404, and Similar For others.

**3-Models:**

Django admin Panel, querSet API , FormAPI, Set up a MySQL database and apply migrations.

**Model:** object equivalent to store ad receive data. **Two ways to work with database is to use:**

**1- the SQL through Application. i.e**

**2-other way is to by creating the model.** Application model Database. Model is The single definitive source information about data. It contains Essentials Fields and behavior’s about data. Generally each table model maps to a single database table. They are integral party Django Framework. Each model is a class of python with Subclasses.

To create th database fields using queries we can do this by model. Django gives the database-access API, we can think model as object of Python. I.e .

**In Django** first-name = models. Charfield (max-length) No need to define PK, it automatically created. To create this, we have to make migrations.

**→ in SQL** ;create Table Tblename ( id,notnull pk; first-name notnull)

To Perform CRUD operations **1-CREATE**

in SQL "insert into user (id, fn, In) values(1, ns),

in Django news user=User (id=1, "', {sher") ;new-user.Save()

**2-READ**

user = user. Objects.get (id=1) Djnago ,**For Update** user.objets.get(id=1);user.last-name=’sher’;user.save()

select\* from tablenamein SQL

**Deletes** user.objects.filer(id=1).delete()in Django

**→After creating model: Make migrations.**

→ and then using Terminal assign the values to the model attributes by running this command as: python manage.py shell.

Also

run these commands as. from Subapp.modelsfile import Modelname;

modelname.objects.all(); modelname.objects. create (fieldname-value)

**Access-\>** p=modelname. objects.get(id=2); P.Fieldname = new-value: p.shows()

**⇒ Migrations:** To make changes in database through model which we have created is called migration. Django provides the CLI to apply migrations, you must create script of migrations then apply migration. **models Script:** set of instructions what to create against database. We apply changes to the model, run the migration file and django will take care of the rest. NoSql required.

**Migrations:** handle syncing, version Control and database maintaince. It acts like version control which keeps history, track changes and remove problems and centralized.

**Make Migrations:** Prepare the changes to be made to a model. **migrate:** Executes Sql commands to make changes to a mode.

**→ To show all the changes run the command:** python manage.py Show migrations.

**To show the detail of migration** : python.manage.py appname 001

**To show the sql behind commit**: python.manage.py sqlmigrate appname 001

There is a Table behind the migration for every updation against migrate.

**⇒ content of migration file:** it is a python code, inside file it's has two List items such as dependencies and operations → **Dependencies:** referred to the previous migration that must applied before this.

**operations:** tre actions to be performed je.. Create model, DeleteModel, Add Field, Alter field, Index. ORM is used to run query against database.

**⇒ Foreign keys:** It is ORM in one model. ORIM can map data between mapped database.

=) Ensure that model should register to admin. 1.py file: admin site.register(modelname)

App.apps. App Config in installed- APPS. You can also explore database file which is sqlite 3

**→ ORM:** As application grows then it automatically creates. It is abstract layer which facilitate interaction between Model and the programing language and database.

ModelORMdatabase

**=\> queryset:** is a collection of objects which are basically our models.

**=) Following Ways:**  methods that return query, operators that return The query and methods that don't return query.

First we have to import the model from database in shell commands . these methods are similar to objects.all()→ select \* ad obj.filter() where ORM it's simple mean that we use code instead of query writing for performing operations on databases.

**⇒ Form:** Django. Forms, HTML form, form Model. Django-form Similar to built in class of form to create form. There is a widget in every-field of form which accepts the additional field.

**in Persistancy.** We can persist the user as formpersist-to-Database to use the app, to solve this problem model can be used which will represent the table which Save the information in db. Model then can be converted into django-form.

**Flow for the form:**  Create form Pass the form to view function use form in html file

**⇒ Model-form**: To Save/retrieve data directly in database From form. Model also provide Model-form class just like model which is used to create the table. i.e.

class Classname (Model form):

class meta:

model = Reservation/model-name or ‘--all—'

Fields = ['name',] field's inside model for form

form =classname() create instance

To Bind the model with form; first import the model which has to bind with form and then add implementation for the model.

Implementation=) To convert the form into model, copy the form code and paste it model file, Then select the code right click and configure it, this will convert to model. Then come to the form file and delete that form code and import the model. here for use rather of form code. Hence this way model form is created from form and it will store the data of form in database automatically, As in The above code. Register the model-form and pass to the views and use in html.

View.py file

def form-view(req):

form = Log form()

if request.method== post:

form = Logform (res. Post) - This will update the db data.

if form.is-Valid():

form.save()

File HTML

{%csrf-token%}

{ form.as-p}

other tags

run migrations

run Server.

This is how model form can be used to create a form and Save form data to correspondence database table.

**Administrative Django:** Trough this Groups and users can be added. First create reservation model, Second add in installed-app (Myapp.myapp.m Apconfig),

3rd Also create Superuser and in admin.py file register model. This reservation model now will be shown in admin panel.

**Permissions:** Control which users are allowed to do which actions. Django has built in authentication ad Authorization.

**There are 3 types of users: Superuser, Staffuser, Enduser**

users can be created by shell command.

python manage.py createsuperuser - username = Ali; -- email- Ali.com

**Permissions**: myapp.add-my-model, myapp. change-mymodel, myapp.delete- mymodel, myApp.view-my- model.

Permissions be check first create user using shell. then Assign the permission. The auth app is added to the installed app to add, change, delete, view permissions.

Permission to specific model can be managed by using admin class. View , add, delete are methods of this class.

**=) User objects:** has two main fields **I-Groups. 2-user**

**User permissions:** Store and reference a single or multiple permission objects. Permission Can be done by the methods set(), add(), remove(), Clear().

**⇒ For Specific Group,** specific permissions are assigned such as for reservation but for superuser all permissions will be transfer to the Change permissions.

Now Add User and assign permission and also assign to a group.

**Django Database options:** By default there is sqlite and no need to configure it. But now We will configure the MySql db. We need db driver all the model to map to db and from db to python queries. Mysqlclient connector is installed to open the connection. In settings.py under the db-option, a config file of all credentials can be set. 1-install db 2-configure of db.

**4-Template:**

Templates and Django Template language, html library integration, debugging and Testing

**Template:** Text-based documents. or python strings marked up using DTL. Django Template Language. DTC contains python code and template engine.

Web frame work often need to generate the dynamic content and to render on html.

**Dynamic Content;** Data that Changes according to context, user behaviour, and preferences.

Templates should passed to the Templates option in settings.py.

**Template Engine:** The Engine that will convert the python code into markup language.

**Template Inheritance:** Template Folder base.html (index.html, ab cut.html)

**Working:** Template Language which is python code and this code is converted into markup Language using template engine.

**DTL consists of** variables {{ }} Tags {% variable % }→ control structure /source of logic.

**Filters:** can Change value of variable {{ string \| upper } }, They also accept argument.

**commits;** {% comment '%} This is a commit {% endcommit %}

**Mapping model objects to templates:** in it, we will use model in view function there the model will be converted to dictionary then this dictionary is passed to view Function.

**⇒ Template inheritance :** it is done to repeat same things by avoiding them to be repeated. So for this inheritance is done i.e base.html([home.html,about.html,menu.html](http://home.html,about.html,menu.html)), in base.html There will be header ad footer and we have to just pass the rest pages between the header and footer.

**For this we use Two Tags:  1- include** in This tag ,the header and Footer will be constant and rest content is passed i.e. {% include 'header.html’%} content{% include "footer.html"}

We also pass the additional arguments along with the view to do the additional task. Include, Render the sub template and include the HTML. Include Can be put many as needed and each has it's own task. It simply includes a template in current context

**2-Extends**: It is similar to the include but it's functionality is different, it allow we to replace the block of content from parent template, It creates a parent child relationship where parent's functionality can be overwritten.

**⇒ It can be used two ways**: 1- It can use the string literal as the name of parent template to be extended. i.e.{% extends ‘base.html’)

2-it Can make use of the value of a variable, once the value is assign to a string, django will use that string as name of parent template. j.e. \<li\> a href= {% url 'home' %}\> Home\</a\>\</li\>

**=)Block of Content:** One file content can be extended to another file content. i.e. in any html file which will Serve as base file write the code {% block content%} {% endblock %} write this line also with which content is to be extended. Also add this line {% extends ‘base.html’ %}, do far all the files which is to be extended. It is similar to include just write the keyword of extends instead of include.

**→ Debugging:** Some errors can benot adding a view, incorrect templates, Missing statement, Inaccessible resources. It is for remove errors.

**⇒ Testing in Django:** It is for quality, reliability and performance. Every framework has many Testing options, i.e. Unit test(function, Class, method) for know this value functionoutput

It is done in tests.py. i.e. class based

import Testcase class, Import modelname

class reservation (Testcase):

def create (self):

Reservation.objects.creat(name = "John', seat-cout=4, tine_atry=leiro)

def test-seat count(self):

customer = Reservation.objects.get(name = "John)

**run this command:** python manage.py test

**or to runall test within a specific Package:** Python manage.py test reservations

**or to run aspecific test case:** manage.py test reservations. tests. Reservationtestcase

**or to run a specific method:** ////// test -seat-Count

on small level project add the file i-e. tests.py

on large project add t the files test-module-py, test-views.py

For implementation: Create model in test.py write test case-

Further Look out the documentation.

1.  **Configuration:**
    -   **Definition:** Configuration refers to the settings, parameters, or options that determine how a system or application behaves.
    -   **Example:** Setting up database connection strings, specifying logging levels, or defining environment variables are part of configuration.
2.  **Integration:**
    -   **Definition:** Integration involves combining different components or systems to work together as a unified whole. It often implies the seamless interaction between these components.
    -   **Example:** Integrating a payment gateway into an e-commerce website or connecting a third-party API to a web application.
3.  **Dependency:**
    -   **Definition:** A dependency is a relationship between two modules or components where one relies on the functionality provided by the other.
    -   **Example:** In software development, a module may depend on a library or external package to perform specific tasks.
4.  **Package:**
    -   **Definition:** A package is a collection of related code or functionalities bundled together for easy distribution, installation, and reuse.
    -   **Example:** In programming, a package might contain a set of classes or functions that provide specific features.
5.  **Injecting:**
    -   **Definition:** Injecting typically refers to the process of providing a dependency to a component or module. Dependency injection is a common technique used in software development to improve modularity and testability.
    -   **Example:** Injecting a database connection object into a service class rather than having the service class create the connection itself.
6.  **Embedding:**
    -   **Definition:** Embedding involves incorporating one component or object into another. It often implies a more intimate connection between the embedded component and its host.
    -   **Example:** Embedding a video player into a web page or embedding an image within a document.

In summary:

-   **Configuration** deals with settings and options.
-   **Integration** involves combining different components or systems.
-   **Dependency** is a relationship where one module relies on another.
-   **Package** is a collection of related code or functionalities.
-   **Injecting** refers to providing dependencies to components.
-   **Embedding** involves incorporating one component into another.



