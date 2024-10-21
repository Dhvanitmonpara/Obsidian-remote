# Docker Notes

## Running Containers

- `docker run -it [image-name]`  
  - `-it` stands for interactive terminal. It creates a new container and opens a terminal session.  
  - Example: `docker run -it ubuntu` (Creates and starts a new Ubuntu container)

- `docker run -it -p [local-port]:[container-port] [image-name]`  
  - Maps ports between the host and the container.  
  - Example: `docker run -it -p 8000:8000 nodejs` (Maps local port 8000 to container port 8000)

- `docker run -it -e key=value -e key=value [image-name]`  
  - Passes environment variables to the container.  
  - Example: `docker run -it -e NODE_ENV=production -e PORT=8000 nodejs`

## Managing Containers

- `docker start [container-name or container-id]`  
  - Starts a previously stopped container.

- `docker stop [container-name or container-id]`  
  - Stops a running container. Alternatively, you can use the `exit` command inside the container terminal.

- `docker container rm [container-name or container-id]`  
  - Removes a container.

## Listing Containers

- `docker container ls`  
  - Lists all running containers.

- `docker container ls -a`  
  - Lists all containers, including stopped ones.  
  - `-a` stands for *all*.

## Executing Commands in Containers

- `docker exec [container-name or container-id] [command]`  
  - Executes a command inside a running container.  
  - Example: `docker exec sharp_elgamal ls` (Runs `ls` inside the `sharp_elgamal` container)

- `docker exec -it [container-name or container-id] bash`  
  - Connects your local terminal to the container's terminal. This allows you to interact with the container directly.  
  - Example: `docker exec -it sharp_elgamal bash`
