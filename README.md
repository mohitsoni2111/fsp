## Initial setup

1. Create project_folder cd into it.
2. `npm create vite@latest` and follow commands.
3. Go back to project_folder.

## Backend

4. Create a Virtual env - `virtualenv env` and activate it.
5. Go back to project_folder. 
6. `pip install django djangorestframework django-cors-headers`
7. `django-admin startproject core`
8. Rename the core to backend `mv core backend`
9. `cd backend`
10. `python .\manage.py migrate`
11. `python .\manage.py createsuperuser`
12. `python .\manage.py startapp posts`
13. Update settings.py file - INSTALLED_APPS and CORS_ALLOWED_ORIGINS
14. Create a Post class in models.py 
15. Register the Post model in admin.py - *admin.site.register(Post)*
16. Create an *api* directory in posts app and inside serializers.py, urls.py, views.py.
17. Edit serializer.py so that we can convert our django model into JSON format to easilt send over web.
18. Also edit the other two .py files.
19. Create *api -> urls.py* in core folder.
20. `python .\manage.py makemigrations`
21. `python .\manage.py migrate`
22. `python .\manage.py runserver`
23. Update the *url.py* under *core*.
24. Now we can create posts either using Django admin UI or using *http://127.0.0.1:8000/api/posts*

## FrontEnd

25. Create an *.env* file.
26. Update the *App.jsx* file.
