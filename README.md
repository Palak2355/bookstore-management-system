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
![Screenshot 2025-04-25 193056](https://github.com/user-attachments/assets/4177a185-277c-4744-a216-27cd83d31422)
![Screenshot 2025-04-25 193155](https://github.com/user-attachments/assets/f2664435-c5cf-4fae-960d-16c8669c6088)
![Screenshot 2025-04-25 193223](https://github.com/user-attachments/assets/10693b37-7dd4-4a78-a9cd-c508f9cd64e7)
![Screenshot 2025-04-25 193249](https://github.com/user-attachments/assets/115b2179-778e-4a78-9904-14466be73e7e)


## Notes
- All forms are manually handled without using Django forms.
- Cart data is stored in user sessions.
- No use of Django's built-in admin interface; a custom admin panel is implemented.

## License
MIT License
"# bookstore-management-system" 
