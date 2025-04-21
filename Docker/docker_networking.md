## Docker Network

* Docker comes with 7 (rumours say there are more) network types.

  1. None
  2. Bridge(Default)
  3. Bridge (User defined)
  4. Host
  5. MACVLAN(Docker swarm)
  6. IPVLAN
  7. Overlay
* **[Docker network Blog](https://dev.to/nobleman97/docker-networking-101-a-blueprint-for-seamless-container-connectivity-3i5b#docker-network-types)**
* by default, docker creates one  **bridge** , **host** and  **null** (none) network each.

Show the docker newtwork list

```bash
$ docker network list
```

###### 1. None Newtwork

container is not attached to any network. container is unable to communicate with any external network or other containers. It is isolated from every other network.

```bash
# running an nginx container in "none" network type
$ docker run -d --network none --name my_nginx nginx
```

###### 2. Bridge (default) Network

The bridge network mode sets up an internal private network within the host. This allows communication between containers within such network, but isolates them from the host's network.

When docker containers are created without specifying a network, they are automatically placed in the *default bridge* network.

```bash
# running a container in the default bridge network
$ docker run -dit --name Rock nginx
```

###### 3. Bridge (user-defined) Network

This network type is similar to the default *bridge (default)* network. It also creates an internal private network within the host, but it does not come already created by Docker. You have to create it yourself.

```bash
# create a user-defined bridge network
$ docker network create -d bridge demo_net
```

```bash
# Attaching containers to bridged network
$ docker run -dit --network demo_net --name service_A nginx

# create another container and publish a port
$ docker run -dit -p 8000:80 --network demo_net --name service_B nginx
```

*service_A* and *service_B* containers are now attached to the 'demo_net' network. By default, all containers within the same network can communicate with one another freely but are isolated from the host network and other user-defined networks.

In order to access applications running on these containers from the host network, we have to publish (or expose) ports from the containers. In the snippet above, port 80 on *service_B* container is mapped to port 8000 on the host, allowing access to an application running on service_B's container port 80 to be accessed from port 8000 on the host.


###### 4. Host Network

Containers in host network mode directly utilize your host's network stack, lacking isolation. They do not receive separate IP addresses, and any port bindings are directly exposed on your host's network interface. In practical terms, if a container process is configured to listen on port 80, it will bind to your host machine's IP address on port 80.

```bash
# bind container to host network
$ docker run -d --network host --name my_nginx nginx
```


* If you're using the host's network for your web container (like Nginx), it means you can't run multiple web containers on the same host and port. This is because they would all share the same network settings, causing conflicts.
