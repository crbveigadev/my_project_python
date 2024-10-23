buildar uma imagem

docker build -t my-app-python .

ver a imagem
docker image ls

rodar o docker
docker run my-app-python

executar o docker
docker ps
docker exec -it xxx bash

parar o containter
docker ps
docker stop xxx

Criar um volume para o desenvolvimento do projeto
docker run -v $(pwd):/app my-app-python

Executar novamente o container
docker exec -it xxx bash

Levantar uma VM e mapeando as portas
docker run -v $(pwd):/app -p 8000:8000 my-app-python

Criando uma nova imagem do Postgres
docker run -e POSTGRES_PASSWORD=root -e POSTGRES_DB=django postgres:15.8-alpine3.20

Verificar o manifesto de uma imagem docker
docker inspect xxx

gerar um ambiente com docker compose
docker compose exec django bash

Remover todas as imagens
docker rmi $(docker images -q)


NA IMAGEM
#Instalar o pipenv
pip install pipenv
export PIPENV_VENV_IN_PROJECT=1

Instalar shell
pipenv shell

Instalar o django
pipenv install django

iniciar o Django
django-admin startproject videos

Rodar a aplicação no DJANGO
python manage.py runserver

Rodar com mapeamento de portas
docker run -v $(pwd):/app -p 8000:8000 my-app-python
python manage.py runserver 0.0.0.0:8000