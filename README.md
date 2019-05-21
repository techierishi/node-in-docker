##### Build Docker image
With the instructions ready all that remains is to run the docker build command, set the name of our image with -t parameter, 
and choose the directory with the Dockerfile:

```bash
$ docker build -t hello-world .
```

##### Run Docker container
The application has been baked into the image. Dinner time! Execute the following string to launch the container and publish it on the host with the same port 8081:

```bash
docker run -p 8081:8081 hello-world
```


##### Sharing Docker image
Docker images can be hosted and shared in special image registries. The most popular is Docker Hub, a GitHub among Docker registries, in which you can host private and public images. Let’s push an image to Docker Hub now:

###### Sign up at hub.docker.com
###### Build the image again using your Docker Hub credentials:

```bash
 $ docker build -t [USERNAME]/hello-world .
```
###### Log in to Docker Hub with your credentials:

```bash
$ docker login
```

###### Push the image to Docker Hub:

```bash
 $ docker push [USERNAME]/hello-world
```
