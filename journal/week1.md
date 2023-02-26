# Week 1 — App Containerization

## Create a Docker file for backend-flask

Following is the Dockerfile that is used to build a Docker image for a backend-flask.

> [Link for Code Commit](https://github.com/snehpalkaur/aws-bootcamp-cruddur-2023/commit/4ab86b9fa9445857585d4ea5d74065ee4ba2c324)

```dockerfile
#Sets the base image for the Docker container.The base image is the official Python 3.10 slim version running on Debian Buster.
FROM python:3.10-slim-buster

#Sets the working directory inside the container to /backend-flask.
WORKDIR /backend-flask

# Copies the requirements.txt file from the local machine to the container's working directory.
COPY requirements.txt requirements.txt

# Installs the dependencies listed in requirements.txt file inside the container using pip3
RUN pip3 install -r requirements.txt

#Copies all the files and folders from the current directory of the local machine to the container's working directory.
COPY . .

#Sets an environment variable named FLASK_ENV with the value development.
ENV FLASK_ENV=development

#exposes the container's port ${PORT} to the outside world
EXPOSE ${PORT}

#Specifies the command to be run when the container starts. It starts the backend-flask by running the flask run
#command with the options --host=0.0.0.0 and --port=4567, which specifies that the application should 
#listen on all network interfaces (0.0.0.0) and the port ${PORT} (default is 4567).
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

```


## Create a Docker file for frontend_react

## Create a Docker Compose file to orchestrate multiple containers

## Create a notification feature for Cruddur

## Implement DynamoDB and PostgreSQL


## Push and tag a image to DockerHub 

> To push and tag a image to Docker Hub, you need to first register an account on Docker Hub. After that, create a repository in DockerHub. Afterwards, build an image on your local machine from DockerFile that you would like to push to the repository you created on Docker Hub. 

In order to push your image to Docker Hub, you need to login on Docker client using the following command: ``docker login --username=yourUsername``

![username](assets/login_d.png)

To tag an image, use this command: ``docker tag imageid username/repositoryname:latest``

![username](assets/d_tag.png)

To push an image to DockerHub, use `` docker push username/repositoryname :latest``

![username](assets/d_push.png)

Finally, you should see an image in your Repository:

![username](assets/d-hub.png)




