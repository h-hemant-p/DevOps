## Installation

we need to install **docker.in** only on server. it provides docker engine, deocker deamon, docker CLI, container D etc.

Command to install Docker

```bash
sudo apt-get install docker.io
```

Command to see status of Docker

```bash
sudo systemctl status docker
```

Command to see the list of Containers

```bash
docker ps
```

Command to add the user to docker group

```bash
# to add current user
sudo usermod -aG docker $USER

# to add user by username
sudo usermod -aG docker <user>

```

Command to refresh the docker group

```bash
newgrp docker
```

Command to login

```bash
docker login
# or
docker login -u <dockerhub_username> 
# then enter the docker hub password or access tocken
```
