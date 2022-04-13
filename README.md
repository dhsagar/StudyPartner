# StudyPartner
A Django based web application to find study partner and share skills.
## Initial setup
Run the following pip install commands on the terminal to install dependency
* $ pip install pillow
* $ pip install mysql-client
* $ pip install django-cors-headers
* $ pip install djangorestframework
## Database
* This project uses mysql database. To use django's default sqlite3 database change the Database section of settings.py file(located in StudyPartner directory)
```
DATABASES = {
     'default': {
         'ENGINE': 'django.db.backends.sqlite3',
         'NAME': BASE_DIR / 'db.sqlite3',
     }
   }
```
* In case of using mysql database create a database named 'study_partner_new_db' as listed bellow.
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'study_partner_new_db',
        'USER': 'root',
        'PASSWORD': 'root',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```
Change USER and PASWORRD if necessary.
## Database migration
* Run the following commands to migrate the database according.
```
$ python manage.py makemigrations
$ python manage.py migrate
```
* This will create all the requred database tables.
## Start project
Run the following command to run the project on the local server 'http://127.0.0.1:8000/'
```
$ python manage.py runserver
```
This takes to homepage of this StudyPartner Project
## Cretae user
* Since the database tables are empty now, create new user by going to the link 'http://127.0.0.1:8000/register'
* Password of new user must be of at least 8 charecters including both alphanumeric and special charecters.
* After logging in create new rooms, explore new room features, write message in the rooms, edit user profile.
### That is pretty much it about the project setup. Explore , add new features and have fun.

## Acknowledgement
This StudyPartner project is done by following a code along django tutorial on youtube for the purpose of learning django framework.
<br>
Youtube link : https://www.youtube.com/watch?v=PtQiiknWUcI&t=24779s&ab_channel=TraversyMedia
