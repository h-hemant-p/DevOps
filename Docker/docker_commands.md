# Docker Commands: From Basic to Advanced

### Basic Docker Commands

##### 1. Checking Docker Version

```bash
docker --version
```

##### 2. Running a Container

```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```

Example:

```bash
docker run hello-world
```

##### 3. Running a Contailer with port mapping and Environment Variables

```bash
docker run -d -p CONTAINER_PORT:LOCAL_DEVICE_PORT -e ENV_VARIABLE1=VALUE1 -e ENV_VARIABLE2=VALUE2 IMAGE_NAME:IMAGE_TAG
```

##### 3. Listing Running Containers

```bash
docker ps
```

4. Listing All Containers

```bash
docker ps -a
```

##### 5. Stopping a Running Container

```bash
docker stop CONTAINER_ID
```

##### 6. Removing a Container

```bash
docker rm CONTAINER_ID
```

##### 7. Removing an Image

```bash
docker rmi IMAGE_ID
```

##### 8. Viewing Container Logs

```bash
docker logs CONTAINER_ID
```

##### 9. Executing a Command Inside a Running Container

```bash
docker exec -it CONTAINER_ID /bin/bash
```

---

### Intermediate Docker Commands

##### 1. Building an Image from a Dockerfile

```bash
docker build -t IMAGE_NAME .
```

##### 2. Listing Images

```bash
docker images
```

##### 3. Running a Container with Port Binding

```bash
docker run -p HOST_PORT:CONTAINER_PORT IMAGE
```

Example:

```bash
docker run -p 5000:5000 my-python-app
```

##### 4. Viewing Docker Events

```bash
docker events
```

##### 5. Docker Container Resource Limits

```bash
docker run --memory=512m --cpus=1 my-app
```

##### 6. Saving and Loading Images

To save an image to a tar file:

```bash
docker save -o IMAGE_NAME.tar IMAGE_ID
```

To load an image from a tar file:

```bash
docker load -i IMAGE_NAME.tar
```

---

### Advanced Docker Commands

#### Docker Compose Commands

##### 1. Starting Services with Docker Compose

```bash
docker-compose up
```

##### 2. Starting Services in Detached Mode

```bash
docker-compose up -d
```

##### 3. Stopping Services

```bash
docker-compose down
```

##### 4. Viewing Logs from Docker Compose Services

```bash
docker-compose logs
```

---

#### Docker Networking Commands

##### 1. Listing Networks

```bash
docker network ls
```

##### 2. Creating a Network

```bash
docker network create NETWORK_NAME
```

##### 3. Connecting a Container to a Network

```bash
docker network connect NETWORK_NAME CONTAINER_NAME
```

##### 4. Disconnecting a Container from a Network

```bash
docker network disconnect NETWORK_NAME CONTAINER_NAME
```

##### 5. Creating a Network  with Specific driver

```bash
docker network create NETWORK_NAME -d DRIVER_NAME
```

---

#### Docker Volume Commands

##### 1. Listing Volumes

```bash
docker volume ls
```

##### 2. Creating a Volume

```bash
docker volume create VOLUME_NAME
```

##### 3. Removing a Volume

```bash
docker volume rm VOLUME_NAME
```

##### 4. Inspecting a Volume

```bash
docker volume inspect VOLUME_NAME
```

---

#### Docker Swarm Commands

##### 1. Initializing a Docker Swarm Cluster

```bash
docker swarm init
```

##### 2. Joining a Node to a Swarm

```bash
docker swarm join --token <SWARM_TOKEN> <MANAGER_IP>:2377
```

##### 3. Listing Swarm Nodes

```bash
docker node ls
```

##### 4. Deploying a Stack in Swarm

```bash
docker stack deploy -c docker-compose.yml STACK_NAME
```

---

#### Docker Secret Management

##### 1. Creating a Docker Secret

```bash
docker secret create SECRET_NAME FILE
```

##### 2. Listing Secrets

```bash
docker secret ls
```

##### 3. Removing a Secret

```bash
docker secret rm SECRET_NAME
```

---

#### Docker Health Checks

##### 1. Adding a Health Check in Dockerfile

```Dockerfile
HEALTHCHECK CMD curl --fail http://localhost:5000/ || exit 1
```

##### 2. Checking the Health of a Container

```bash
docker inspect --format '{{json .State.Health}}' CONTAINER_ID
```

Note: 

```
-d # used for the run in background
-p # used for specify the port
-e # used Environment variables

```
