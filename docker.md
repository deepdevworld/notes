
# Docker important commands
***
* **if permision issue occurs shown below while running docker-compose up us the command:  ***
```
sudo chmod 666 /var/run/docker.sock
```
```
raise DockerException(docker.errors.DockerException: Error while fetching server API version: ('Connection aborted.', PermissionError(13, 'Permission denied'))
```
***
* ***command to connect to the database running in container from the local machine:  `docker exec -it <postgres_container_name> psql -U postgres`***

* ***

# To open the terminal for a database running in a docker

* docker exec -it `database name` psql -U postgres
```
docker exec -it database_with_docker_postgres_1 psql -U postgres
```