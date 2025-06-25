# Django Internship Assignment

## Features

- Django REST Framework with public & protected API endpoints
- Token Authentication
- Celery for background task (email sending)
- Telegram bot integration to collect usernames
- Login page

## Setup Instructions

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
python manage.py migrate
python manage.py createsuperuser
celery -A internship_project worker --loglevel=info
python manage.py runserver
```

## API

- `/api/public/` - public access
- `/api/protected/` - token required
- `/api/login/` - login view
