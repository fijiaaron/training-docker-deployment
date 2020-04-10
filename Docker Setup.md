Docker Setup
============

Download & Install Docker Desktop
---------------------------------

1. Download and install Docker Desktop to your workstation:

https://docs.docker.com/get-docker/


Register at Docker hub
-----------------------

2. Register at Docker hub so you can search for Docker images:

https://hub.docker.com/signup


Test your docker installation
-----------------------------

	docker version

	docker info
	
    docker run hello-world


Register on Docker Hub
-------------------------

https://hub.docker.com/signup


Install a docker image and run it
---------------------------------

Ubuntu Linux

	docker run -it ubuntu:latest bash

Alpine Linux (a lightweight distrobution)

	docker run -it alpine ash

Command options

	docker run --help


Exercise: run a web server 
--------------------------

	docker pull nginx:latest
	docker run --name training -v .:/usr/share/nginx/html:ro -p 8888:80 nginx

http://localhost:8888/


Creating a Docker image
-----------------------

Introducing the Dockerfile

	FROM nginx:latest
	RUN cp src/ /usr/share/nginx/html
	EXPOSE 80

Create a src folder and add an HTML document:
	
	mkdir src
	echo "<html><body><h1>Hello Docker</h1></body></html>" > src/index.html
	
Build your Docker image

	docker build -t mycontainer .

Run it 

	docker run mycontainer 

Managing containers and images
------------------------------

See images

	docker images

See all images

	docker images -a

See running containers

	docker containers ls

Stop a container

	docker stop <container name>

Remove an image

	docker rmi <image>

	docker container ls



