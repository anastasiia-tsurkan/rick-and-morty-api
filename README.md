# rick-and-morty-api

### How to run:
- Create venv: `python3 -m venv venv`
- Activate venv on Windows: `venv/Scripts/activate`
- Activate venv on Unix: `source venv/bin/activate`
- Install requirements: `pip install -r requirements.txt`
- Run migrations: `python3 manage.py migrate`
- Run Redis server: `docker run -d -p 6379:6379 redis`
- Run celery for tasks handling: `celery -A rick_and_morty_api worker -l INFO`
- Run celery beat for task scheduling: `celery -A rick_and_morty_api beat -l INFO --scheduler django_celery_beat.schedulers:DatabaseScheduler`
- Create schedule for running sync in DB
- Run app: `python3 manage.py runserver`
