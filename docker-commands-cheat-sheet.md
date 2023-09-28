# Docker Commands Cheat Sheet
---

## Running docker containers

Usage | Command
------|--------
Run docker image in interactive mode	| docker run -it image-name:image-tag  
Run docker image in interactive mode with host port 8080 mapped to container port 80 | 	docker run -it -p 8080:80 image-name:image-tag
Run docker with the 3001 port exposed | 	docker run -it --expose=3001 
Run docker container with an environment variable set	| docker run -it -e RUST_BACKTRACE=1 image-name:tag-name
Run a docker command in container and remove container after finishing |	docker run --rm -it --expose=3001 image-name:tag-name
Run docker container as a daemon process	| docker run -d image-name:tag-name
Run shell with docker alpine image	| docker run -it --rm alpine sh
Start  a container by name	| docker start container-name
Stop a container by name	| docker stop container name 
Run commands inside a running docker container e.g. shows `ls` in a running container | docker exec -it 4a140740c577 ls

## Checking docker resources

Usage | Command
------|--------
Check docker images	| docker images / docker images ls
Check docker containers	| docker ps -a / docker container ls
Check the process running inside the container	| docker top container-name or container-id
Check resource utilization	| docker stats
Check docker logs with multiple time options	| docker logs -f --since <1s|5m|1d|UTC date time container-name
Inspect container configurations	| docker inspect
docker show disk information	| docker system df
docker show system events	| docker system events 
docker show system info	| docker system info
docker prune unused data	| docker system prune
Snoop network settings of a running container	| docker inspect $container_id | $container_name
Check docker image content, if entrypoint is provided	| docker run -it --entrypoint sh image-name


## Updating docker container resources
Usage | Command
------|---------
Update container configurations and restart	| docker update --restart=always container-name
Update container configurations	| docker update --kernel-memory 80M container-name

## Cleanup docker containers	
Usage | Command
------|--------
Cleanup stopped containers   | docker rm $(docker ps -q -f 'status=exited')
Cleanup dangling images	| docker rmi $(docker images -q -f "dangling=true")
Cleanup dangling volumes	| docker volume rm $(docker volume ls -qf dangling=true)
Cleanup all unused docker artifacts	| docker system prune
Cleanups docker containers | docker container prune
Cleanup docker images | docker image prune
Cleanup unused networks | docker network prune
Cleanup unused volumes | docker volume prune



