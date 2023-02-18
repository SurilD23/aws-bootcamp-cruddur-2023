FROM python:3.10-slim-buster

# Inside Container
# make a new folder
WORKDIR /backend-flask

# Outside Container -> Inside Container
# Install libs
COPY requirements.txt requirements.txt

# Inside Container
# Install python libs
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# . means everything in the current dir
COPY . .

# set env vars
ENV FLASK_ENV=development

EXPOSE ${PORT}
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]