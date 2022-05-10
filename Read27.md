# Using Django models 
- Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.
- The definition of the model is independent of the underlying database — you can choose one of several as part of your project settings. Once you've chosen what database you want to use, you don't need to talk to it directly at all — you just write your model structure and other code, and Django handles all the dirty work of communicating with the database for you.
- The models are basically a representation of your application’s database layout.
- All models are subclass of the `django.db.models.Model` class. Each class will be transformed into database tables. Each field is represented by instances of `django.db.models.Field` subclasses (built-in Django core) and will be translated into database columns.
- One way to create a relationship between the models is by using the `ForeignKey `field. It will create a link between the models and create a proper relationship at the database level. The `ForeignKey` field expects a positional parameter with the reference to the model it will relate to.

# Migrating the Models
The next step is to tell Django to create the database so we can start using it.

Open the Command Line Tools, activate the virtual environment, go to the folder where the manage.py file is, and run the commands below:\
```
python manage.py makemigrations
```
As an output you will get something like this:\
```
Migrations for 'appname':
  boards/migrations/0001_initial.py
    - Create model Board
    - Create model Post
    - Create model Topic
    - Add field topic to post
    - Add field updated_by to post
```
At this point, Django created a file named `0001_initial.py `inside the appname/migrations directory. It represents the current state of our application’s models. In the next step, Django will use this file to create the tables and columns.

The next step now is to apply the migration we generated to the database:
```
python manage.py migrate
```

The output should be something like this:

```
Operations to perform:
  Apply all migrations: admin, auth, boards, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying boards.0001_initial... OK
  Applying sessions.0001_initial... OK
  
```