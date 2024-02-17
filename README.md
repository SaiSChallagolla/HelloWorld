# Helloworld Application Instructions in windows
## Step1-Checking Django version
check whether django is installed in your system by using below command:

```py -m django --version```

## Step2-creating project
by using cd command change the destination folder at where project has to be stored then use the below command to create "HelloWorld" Application.

```django-admin startproject HelloWorld```

by running the above command you can observe a "HelloWorld" folder is created , which contains below  files
```
    manage.py
    HelloWorld/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```
## Step-3 Running Server 
use below command to run the server

```py manage.py runserver```

After running you observe output in cmd as follows:

```
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
February 17, 2024 - 00:02:01
Django version 5.0.2, using settings 'HelloWorld.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.
```
## Step-4 creating pools app
now change your directory into "HelloWorld" by using "cd" command and run the below command:

``` py manage.py startapp polls ```

After running above command you can observe a new "pools" folder is created, which contains the below files

```
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```
## Step-5: Adding code

Now we need to modify the views.py file code as follows:
``` python
from django.shortcuts import render
from django.http import JsonResponse

# Create your views here.
def index(request):
    return JsonResponse({'Message': 'Hello World!'})
```
Now create a "urls.py" python file and add the following code in it
``` python
from django.urls import path

from . import views

urlpatterns = [
    path("", views.index, name="index"),
]
```
Now modify HelloWorld/urls.py file as follows
``` python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path("polls/", include("polls.urls")),
    path("admin/", admin.site.urls),
]
```
## Step-7 Running Server
Now run the server again by using command

```py manage.py runserver```
Now go to "http://localhost:8000/polls/ " website it shows the output as follows:

```
{"Message": "Hello World!"}

```








