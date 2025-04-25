# Bookstore Management System

## Project Overview
This is a full stack Python Django application for managing a bookstore. It includes user authentication, a custom admin panel for managing books, and a session-based shopping cart. The application is fully dockerized and includes a Jenkins pipeline for CI/CD automation.

## Features
- User Registration and Login/Logout using class-based views and manual HTML forms.
- Custom Admin Panel (no Django admin) for adding, editing, and deleting books.
- Book listing and detailed book pages.
- Add to Cart functionality using Django sessions.
- Dockerized environment with docker-compose.
- Jenkins pipeline for automated build, test, and deploy.

## Tech Stack
- Python 3.10
- Django 4.x
- PostgreSQL (via Docker)
- Docker & Docker Compose
- Jenkins for CI/CD
- Gunicorn as WSGI server

## Setup & Run Instructions

### Prerequisites
- Docker and Docker Compose installed
- Jenkins installed (optional for CI/CD)

### Running Locally with Docker
1. Build and start the containers:
   ```
   docker-compose up --build
   ```
2. Apply migrations:
   ```
   docker-compose run web python manage.py migrate
   ```
3. Create a superuser (optional for admin access):
   ```
   docker-compose run web python manage.py createsuperuser
   ```
4. Access the app at `http://localhost:8000`

### Jenkins Pipeline
The Jenkinsfile is configured to:
- Build the Docker image
- Run Django tests
- Deploy the application using docker-compose

## Screenshots
*(Add screenshots here if available)*

## Notes
- All forms are manually handled without using Django forms.
- Cart data is stored in user sessions.
- No use of Django's built-in admin interface; a custom admin panel is implemented.

## License
MIT License
"# bookstore-management-system" 
