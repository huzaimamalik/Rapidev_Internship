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
