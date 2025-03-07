# Task_Manager

##first you need to ensure that the following are installed in your laptop:
such as Phyton,Pip,Virtual Environment,Django and mysqlclient.


so first step is to install pip and virtual env

pipenv install django
pipenv shell
pip install mysqlclient

second is setting up the django project
create a django project and a app within that project then run the following commands on your terminal:

django-admin startproject project_name
cd project_name
python manage.py startapp app_name

third is to register app and database
include app in the installed_apps list:

INSTALLED_APPS = [
'myapp,
]

mysql database

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql', <!--Specifies that MySQL is the database backend-->
        'NAME': 'ad_tasklist', #Name of the database
        'USER': 'root', #Database username
        'PASSWORD': '', #Database password
        'HOST': 'localhost', #Database host
        'PORT': '3306', #Default MySQL port
    }
}

fourth one is to define the models 
after creating the models, run the following commands to create migration

python manage.py makemigrations
python manage.py migrate

fifth one is to set up the templates, urls, forms, and etc.
after that navigate the project directory.

cd project name

next step is start the development server

python manage.py runserver

right after that is to click the link "(http://127.0.0.1:8000/)

project set up is done, now you can test it.
