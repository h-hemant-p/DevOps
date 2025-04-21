## Docker File

* All lines are executes at the time of build the image except **CMD**.
* **CMD** is used to run the container. it means **CMD** invokes only when we run the container.
* We can Override the command **CMD** at the time ot run the container.
* **ENTRYPOINT** is also like **CMD** but it can't be override.



**Docker file for a basic NodeJs app**

```bash
# pull a base image which gives all required tools and libraries
# pull nodejs 22 image
FROM node:22

# create a folder where the app code will be stored
# set working directory
WORKDIR /app

# copy the source code from your HOST machine to your Container
COPY . .

# install dependencies
RUN npm install

# expose the port
EXPOSE 3001

# run the application
CMD ["npm","start"]

```
