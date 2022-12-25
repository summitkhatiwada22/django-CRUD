### django-tutorial

### check if you have both python and pip installed
`python --version`
`pip --version`

### create a virtual environment and activate it
`python -m venv <env name>`
`source <env name>/bin/activate`

### install Django framework and check django version
`python -m pip install Django`
`django-admin --version`

### create a django project and run
`django-admin startproject <project name>`
`python manage.py runserver`

### create a django app
`python manage.py startapp <app name>`

### django views
1. from django.http import HttpResponse
2. `def index(request):
       return HttpResponse("content")`
3. create urls.py in app level where you have views.py
4. from . import views
5. define urlpattens
6. define app and url in main level

### django templates
1. create templates folder under the app level i.e. members
2. write html code under a file inside template
3. under views, from django.template import loader
4. load the template using
    `template = loader.get_template('<template name>')
     return HttpResponse(template.render())`

### tell django new app is created by adding on INSTALLED_APPS[] under settings
'members.apps.MembersConfig'

### migrate
`python manage.py migrate`

### django models
1. under models.py in app level, add a class Members(models.Model)
2. add class attributes for database
    `firstname = models.CharField(max_length=255)
     lastname = models.CharField(max_length=255)`
3. run the following code to make migration of new model
    `python manage.py makemigrations members`
   
make model class -> `python manage.py makemigrations <app name>` -> `python manage.py migrate`

