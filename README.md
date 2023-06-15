mkdir django_docker_base

cd django_docker_base/

git clone https://github.com/iago-mansur/django_docker_model.git

code .

criar Dockerfile, docker-compose.yml, requirements.txt, .gitignore, pasta app

sudo chmod 666 /var/run/docker.sock

docker build .

docker-compose build

docker-compose run --rm app sh -c "django-admin startproject app ."

docker-compose up

http://127.0.0.1:8000/

editar docker-compose.yml

editar requirements.txt

docker-compose down

docker-compose build

editar app/app.settings.py

docker-compose run --rm app sh -c "django-admin startapp core"

delete test.py views.py 

criar app/core/tests/__init__.py

editar setting

criar app/core/management/__init__.py

app/core/management/commands/__init__.py

criar app/core/management/commands/wait_for_db.py

criar app/core/tests/test_commands.py

docker-compose run --rm app sh -c "python manage.py test"

editar app/core/management/commands/wait_for_db.py

docker-compose run --rm app sh -c "python manage.py test"

docker-compose run --rm app sh -c "python manage.py wait_for_db"

editar docker-compose.yml

docker-compose down

docker-compose up

http://127.0.0.1:8000/