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