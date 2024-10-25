# Project management API
A Django REST framework app is used for project management.

## Table of Contents
- [Features](#features)
- [Used technology](#used-technology)
- [How to Run Development Server](#how-to-run-development-server)
- [Documentation](#documentation)

## Features
- **User Management**: Create, delete, and update users, projects, departments, and clients.
- **Department Assignment**: Assign users to specific departments and establish an operational order.
- **Task Management**: Track tasks with options to start, pause, or complete them.
- **Paginator**: Paginator is used in project and task views to perform database queries faster.
- **File Management**: Upload and assign files to departments, creating a technological path.
- **Real-Time Notifications and updates**: Notifications via WebSocket for administrators (all project and task updates) and users (assigned tasks).

## Used technology
- daphne>=4.1.0,<4.2
- uwsgi>=2.0.24,<2.1.0
- psycopg2>=2.9.7,<2.10
- Django>=5.0.3,<6.0
- django-cors-headers>=4.4.0,<4.5
- djangorestframework>=3.15.0,<3.16
- channels>=4.1.0,<4.2
- redis>=5.0.0,<5.1
- channels-redis>=4.2.0,<4.3
- drf-spectacular>=0.27.1,<0.28
- Pillow>=10.4.0,<10.5.0

## How to run development server
**Requirements**: Ensure you have [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/) installed.

In the main project folder, run the following commands:
In main folder type:
- `docker-compose build`: Builds the Docker images.
- `docker-compose up`: Starts the server.
- `docker-compose run --rm app sh -c "python manage.py createsuperuser"`: Sets up an admin user for the application.

## Documentation
Full API documentation is available at [http://localhost:8000/api/docs/](http://localhost:8000/api/docs/).
