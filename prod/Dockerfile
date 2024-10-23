FROM python:3.12.6-slim

# pipenv - npm for python
#ENV PIPENV_VENV_IN_PROJECT 1
RUN pip install pipenv

#Criar user para que não seja root na imagem
RUN useradd -ms /bin/bash my-user

#Utilizar um usuario nao root
USER my-user

#Configurar o workdir
WORKDIR /app

#Chown app
RUN chown -R my-user /app

#Copy
COPY --chown=my-user:my-user . /app

#Comando que será executado ao iniciar o container
CMD ["tail", "-f", "/dev/null"]



