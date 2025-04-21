## Docker Image and Container

Docker Image is blue print for creating a container.

Docker container is a .....

* **Docker File** - contains the step by step instructions to build an docker image.
* Docker File-> (build) -> Docker Image ->(run) -> Docker Container
* Docker also provides pre-build Images.
* When ever we change the code we need to update(re-build) the image.



Pull the image from docker hub or public images

```bash
docker pull <image_name>
```

Build an dockerfile to create Image

```bash
docker build -t <name_for_the_image> .

# . -> path of dockerfile
```

See the list of docker Images

```bash
docker images
```

Run docker Image

```bash
docker run <image_name>
```

Run a Image in background 

```bash
docker run -d <image_name>
# -d -> datach
```

If I run directly and image then docker first pull the image then run this image

```bash
docker run hello-world 
# hello-world is a public image
```

Command to see the list of Containers

```bash
docker ps
```

Stop an container

```bash
docker stop <container_id>
```

Delete docker image

```bash
docker rmi <image_id>
```

Set environment variable at time of running image

```bash
docker run -e <variable_1> = <value_1> -e <variable_2> = <value_2> <image_name>

# Example
docker run -e JWT_SECRET_KEY=823u73hhgrfej82 -e MONGODB_URI=mongodb://localhost:27017 my-app 
```

Port mapping at the time of run the Image

```bash
docker run -d -p <host_port>:<container_port> <image_name>

# -p -> publish 

# example 
docekr run -d -p 3001:3001 my_app
```

See the logs of container

```bash
docker logs <container_id>
```

Attach the terminal with container

```bash
docker attach <container_id>

# it helps to see the logs in realtime (but screen will be blocked) you need to stop container from another terminal then logs terminal will be free automatically.
```

Create interactive terminal for an container

```bash
docker exec -it <container_id> bash
```

Keep an container always in running status

```bash
docker run -itd <image_name>

# Example
docker run -itd ubuntu
```
