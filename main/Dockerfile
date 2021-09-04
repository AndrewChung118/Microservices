# Using Requirements
# FROM python:3.8

# WORKDIR /app

# COPY requirements.txt ./
# RUN pip3 install -r requirements.txt

# COPY . ./

# # "--host=0.0.0.0" - sets docker to run on local host
# CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]

FROM python:3.7-slim

ENV CONTAINER_HOME=/app
WORKDIR $CONTAINER_HOME

# RUN pip install -r $CONTAINER_HOME/requirements.txt
RUN pip install --upgrade pip
RUN pip install pipenv

# Copy pip files
COPY Pipfile* .

# install dependencies
RUN pipenv install --dev --system --deploy

# copy the rest of files over
COPY . .

CMD gunicorn --bind 0.0.0.0:8000 --workers 4 "main.app:create_app()"