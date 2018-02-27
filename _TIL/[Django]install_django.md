---
layout: post 
tag: Django
title: Install Django
date: 2018.02.27
---

## Install Django  
Django is **python web framework**. So, you need to install python before installing django.  
You can download python from below site  
```
https://www.python.org/downloads/
```
  
There are **two versions** for python   
According to your style, download either 2.x version or 3.x version  
  
After downloading python, you also must download django **through pip**.    
**Pip is download tool** for Python package   
You can download django by typing below command   
```
pip install django
```
  
Now, you can use django web frame work.  
To make your first app, type below command
```
django-admin startproject my_project
```
  
If you want to start your first app, type below command  
```
cd my_project //enter my_project
python manage.py runserver 0.0.0.0:80
```
  
You can see your web application is excuted at http://localhost   