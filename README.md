# MyProject - Django Auth + CRUD App

Simple Django application demonstrating user authentication and CRUD operations.

## Tech Stack
- Django 5.0.6
- SQLite (default DB)
- Bootstrap 5 (CDN)

## Apps
- `user` - handles registration, login, logout, profile view/edit
- `myapp` - handles CRUD operations on Item model

## Setup Instructions

1. Create and activate a virtual environment:
   python -m venv venv
   source venv/bin/activate   (Linux/Mac)
   venv\Scripts\activate      (Windows)

2. Install dependencies:
   pip install -r requirements.txt

3. Create the Django project structure (if not already present):
   django-admin startproject myproject .
   python manage.py startapp user
   python manage.py startapp myapp

4. Place all provided files into their respective paths as shown in the folder structure.

5. Create a `templates` folder in the project root and add all template files.

6. Apply migrations:
   python manage.py makemigrations
   python manage.py migrate

7. Create a superuser (optional, for admin access):
   python manage.py createsuperuser

8. Run the development server:
   python manage.py runserver

9. Visit http://127.0.0.1:8000/ in your browser.

## Features
- User registration and login/logout
- Profile view and edit (bio, phone, location)
- CRUD operations on Items (create, list, view, update, delete)
- Items are scoped per logged-in user
- Bootstrap-based responsive UI with parent-child template inheritance (base.html)

## Notes
- Update `SECRET_KEY` and `DEBUG` settings before deploying to production.
- SQLite is used by default; switch `DATABASES` in settings.py for production databases.
