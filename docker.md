Managing Images
	--Download an image from Docker
	docker pull image_name
	--List all images saved on your machine
	docker images
	--Delete an image
	docker rmi image_name

Running Containers
	--Basic Run Command
	docker run image_name

Viewing and Managing Containers
	--List actively running containers
	docker ps
	--List ALL containers
	docker ps -a

Start, Stop, or Restart a container:
	docker stop container_name_or_id
	docker start container_name_or_id
	docker restart container_name_or_id

Delete a stopped container
	docker rm container_name_or_id

Interacting with Containers
	docker exec -it container_name_or_id /bin/bash

View the logs
	docker logs container_name_or_id

The Cleanup Command
	docker system prune
	--We can add -a to the end to also delete ALL images that aren't currently attached to a running container

Creating Custom Docker Containers
	Step 1: Create Your Workspace
		mkdir customContainer
		cd customContainer
		--make a script in this directory and add whatever commands you want to execute...
		Example:
		#!/bin/sh
		echo "Hello from my custom Hacker container!"
		--we write this in script.sh

	Step 2: Write the Dockerfile
		nano Dockerfile
		FROM ubuntu:latest --sets up the environment by getting a fresh image of ubuntu
		COPY script.sh /script.sh --copies the script to the root directory
		RUN chmod +x /script.sh --give execute permissions for the script
		CMD ["/script.sh"] --this tells the docker that the command next to CMD is to be executed

	Step 3: Build Your Custom Image
		docker build -t my-custom-app .
		--makes the custom image in the current directory

	Step 4: Run Your Custom Container
		docker run my-custom-app
		--runs the custom container
