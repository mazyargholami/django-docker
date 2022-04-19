# django-docker

## Deploying django with docker compose (Test database, Static file, Media file).

---

### Requirements
`Python`

`Nginx, Postgresql`

`Django, psycopg2, uWSGI`

---


#### Run automatically:

`python manage.py wait_for_db`

`python manage.py collectstatic --noinput`

`python manage.py migrate`

---

### System:
`docker-compose up`

port: 8000

---

### Server:
`docker-compose -f docker-compse-deploy.yml up`

port: 80

---

### Example

`docker-compose -f docker-compose-deploy.yml run --rm app sh -c "python manage.py createsuperuser"`

