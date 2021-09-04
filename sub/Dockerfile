# # Using Pipenv
# FROM python:3.8

# # Set ENV
# ENV FLASK_APP=sub_app.py
# ENV CONTAINER_HOME=/var/www

# ADD . $CONTAINER_HOME
# WORKDIR $CONTAINER_HOME
# # Create workspace ./app
# # WORKDIR /app/sub


# RUN pip install --upgrade pip
# RUN pip install pipenv

# # Copy pip files
# COPY Pipfile* .

# # install dependencies
# RUN pipenv install --dev --system --deploy

# # copy the rest of files over
# COPY . .

# # # "--host=0.0.0.0" - sets docker to run on local host
# # CMD flask run --host=0.0.0.0 --port=5001
# CMD gunicorn -w 3 -b :5001 -t 30 --reload wsgi:app

FROM python:3.7-slim

ENV CONTAINER_HOME=/var/www2

ADD . $CONTAINER_HOME
WORKDIR $CONTAINER_HOME

RUN pip install -r $CONTAINER_HOME/requirements.txt