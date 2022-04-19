# django-docker

### Deploying django with docker compose. (Test database, Static file, Media file)


- Django + psycopg2 + uWSGI

#### Requirements in docker:
    Python

    Nginx, Postgresql


---


#### Run automatically:

    python manage.py wait_for_db

    python manage.py collectstatic --noinput

    python manage.py migrate

---

#### Run in system:

  `port: 8000`

    docker-compose up  


---

### Run in server:

  `port: 80`

    docker-compose -f docker-compse-deploy.yml up -d

---

#### Example code:

    docker-compose -f docker-compose-deploy.yml run --rm app sh -c "python manage.py createsuperuser"
