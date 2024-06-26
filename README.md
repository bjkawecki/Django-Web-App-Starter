# A starter for your next Django web app


![Static Badge](https://img.shields.io/badge/Django-%23092E20?style=for-the-badge&logo=django&logoColor=white)
![Static Badge](https://img.shields.io/badge/Poetry-%2360A5FA?style=for-the-badge&logo=poetry&logoColor=white)
![Static Badge](https://img.shields.io/badge/Docker-%232496ED?style=for-the-badge&logo=docker&logoColor=white)
![Static Badge](https://img.shields.io/badge/PostgreSQL-%234169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Static Badge](https://img.shields.io/badge/Celery-%2337814A?style=for-the-badge&logo=celery&logoColor=white)
![Static Badge](https://img.shields.io/badge/Redis-%23DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Static Badge](https://img.shields.io/badge/Tailwind%20CSS-%2306B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Static Badge](https://img.shields.io/badge/Htmx-%233366CC?style=for-the-badge&logo=htmx&logoColor=white)
![Static Badge](https://img.shields.io/badge/Material%20Design%20Icons-%232196F3?style=for-the-badge&logo=materialdesignicons&logoColor=white)


This is some boilerplate code, that I pieced together for my latest Django project.

Alongside a predefined development setup, you will find some helpful features to  get you started quickly for creating your next Django web application.

## Prerequisites

- Python 3.12
- PostgreSQL 16.2
- Docker 26.1
- Docker Compose 2.27


## Features

### Django
- Allauth
- Custom User Model
- Split settings
- Context processor for global variables
- Logger
- Poetry with development dependencies in extra group
- Environment variables for secure configuration

### Client
- Tailwind CSS with Flowbite
- HTMX
- Some templates with a predefined layout
- A landing page

### Convenience

Use the `Makefile` to shorten common and often used comands.

For example `poetry run python manage.py makemigrations` becomes `make mm`.

### Lint
You can lint your files with pre-commit `poetry run pre-commit run --all-files`.
First time will install the hooks from .pre-compose-config.yaml.
Shortcut in Makefile: `make lint`

If you want to use `pre-commit` with `git`, you need to activate a virtual environment.

First, create the virtual environment. On GNU/Linux you do this by

`python -m venv .venv`

and activate it by

`source .venv/bin/activate`

In the first run, pre-commit will update your projects files according to your configuration.

For your django-templates files you can use djlint with `djlint . --reformat`


## How to get started

Build the docker containers:

```
$ docker-compose -f docker-compose.dev.yaml build
```

Install the node modules:

```
$ npm install
```

Start the docker containers in the background:

```
$ docker-compose -f docker-compose.dev.yaml up -d
```

Update your Tailwind css file:

```
$ npx tailwindcss -i ./static/css/input.css -o ./static/css/output.css --watch
```

See your developtment server at `http://0.0.0.0:8000/`. You can hook into the django container:

```
$ docker exec -it django_starter_web bash
```
