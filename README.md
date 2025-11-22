# Simple Python Flask Dockerized Application #

Build the image using the following command
(Here the docker image is created with name "pythonfirst" and tag "v1" from dockerfile present in current directory)

```bash
$ docker build -t pythonfirst:v1 .
```
Check the image created by using command,

```bash
$ docker images
```

Run the Docker container using the command shown below.
(Here the docker engine will run the container from image pythonfirst:v1 in detached mode and with port mapping 5000:5000 )

```bash
$  docker run -d -p 5000:5000 --name pythonfirstdocker pythonfirst:v1
```

The application will be accessible at http:127.0.0.1:5000
In my machine I am using a self hosted Ubuntu VM(Inside Proxmox VE) in which the docker is running so I am able to access the application using VM's IP (http://192.168.1.190:5000/)

