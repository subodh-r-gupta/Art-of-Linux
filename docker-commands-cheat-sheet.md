# Docker Commands Cheat Sheet
---

## Run docker containers

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
