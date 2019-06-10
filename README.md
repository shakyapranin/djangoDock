# Django environment in docker

This is a basic django installation with services isolated in docker containers. Use of TastyPie library for easy API constructions.

## Requirements
   - [Docker](https://www.docker.com/)
   - [Docker Compose](https://docs.docker.com/compose/)

## Getting started
		Inside the directory run 
			- $ docker-compose build once
		For all future runs
			- $ docker-compose up -d
		To view all docker containers run
			- $ docker ps
		
		To execute commands from inside a docker container
			- $ docker exec -it webserver bash

## Project migrations

		From the docker container run
			- $ python3 manage.py makemigrations
			- $ python3 manage.py migrate

## Project Access

		- The postgres admin can be accessed on the port 9000.
		- The application will be accessible on the port 8000.
		- Post gres database is exposed on the port 5432.

	The above configurations can be modified from the docker-compose.yml file itself.


## Create your custom django application by
		- sudo docker-compose run web django-admin startproject <project_name> .