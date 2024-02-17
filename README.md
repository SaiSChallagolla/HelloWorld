# Helloworld Application Instructions
## Step1-Checking Django version
check whether django is installed in your system by using below command:

In windows

```py -m django --version```  or

if you are using linux use command

``` python -m django --version```

if django version is not showing then use below commands to install django:
In windows

```py -m pip install Django```

In Linux:

```python -m pip install Django```

## Step2-creating project
by using cd command change the destination folder at where project has to be stored then use the below command to create "HelloWorld" Application.

Windows command:

```django-admin startproject HelloWorld```

Linux Command:

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
