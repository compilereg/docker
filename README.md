# docker
Different docker related files such as (docker-compose, and Dockerfiles)
docker-compose: A directory contains different docker-compose files to create multi-container application
Dockerfile: A directory contains different Dockerfiles to create different docker images

docker-compose/wordpress/
docker-compose.yml: Is a docker-compose file creates a wordpress container that uses a volume to mount the wp-content directory.
prerequisite:
	A network called wordpressnet with subnet 192.168.10.0/24
	A Volume called ahmedwordpress to store the wp-content directory
	The container name may be chaned in container_name
	To publish the container,uncomment ports scope.
