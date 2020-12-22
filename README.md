# django-gunicorn-nginx-docker

## Usage

```
$ docker-compose up -d --build
$ docker-compose exec web python manage.py flush
$ docker-compose exec web python manage.py makemigrations
$ docker-compose exec web python manage.py migrate
$ docker-compose exec web python manage.py createsuperuser
```