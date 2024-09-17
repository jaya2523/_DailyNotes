Containers, Docker, Docker Compose
Docker Registry
Kubernetes
-pods
-Workloads
-Services
-Updates
-Storage
-App Settings
-Observability
-Scaling

--
Microservices Concept
--
A variant of the service-oriented architecture(SOA) structural style-arranges an application as a collection of loosely coupled services.

In a microservices architecture, services are fine-grained and the protocols are lightweight.
autonomous

---
Monolithic Architecture
--

Built as single unit
Deploy as a single unit
Duplicated on each server
3-tier app -> Web, Buisness, Data

--
From Monolithic to Microservice
--
Use strangler pattern

By handling failures this way, Kafka ensures that your data (like your order details) is always available and processed correctly, even if some servers are temporarily unavailable. This makes Kafka very reliable for handling important and continuous data streams.

--
Microservices Anti Patters
--

--
Microservices drawbacks
--
Latency issues
Transient Errors

--
Cloud Native
--
• Within a short time, cloud native has become a driving trend in the software industry
• It's a new way to think about building complex systems
• Takes full advantage of modern software development practices, technologies, and cloud infrastructure
• Widely popular in the open source communities

explify the approach to <br>
Container, Service, Meshes, Microservice, Immutable Infrastructure and Declaritive APIs.

<b>1. Containerization</b>
<b>2. CI/CD </b>
<b>3. Orchestration </b>
<b>4. Observability and Analysis </b>
<b>5. Service Proxy, Discovery, & Mesh</b>
<b>6. Networking, Policy nd Security</b>

--
pulling images from the v2 which means to fetch the image from web not from cache
--

Container regisrty->docker hub

--
Docker
--
Provides container runtime

--
Docker cli cheat sheet 
--
<h1>1. management </h1>
**docker info**
**docker version**
**docker login** - default we logged in to docker registry and using this command we logged to docker hub.

<h1>2. Running and stoping image</h1>
docker pull [imageName]
docker run [imageName]
docker run -d [imageName]
docker start [containerName]
docker ps
docker ps -a 
docker stop [containerId]
docker run [containerId]
dock kill [containerId]
docker image inspect [imageId]

<h1>3. Running a Container</h1>
<h4>pull and run an nginx server</h4>
docker run --publish 80:80 --name webserver nginx

<h4>list the running containers</h4>
docker ps

<h4>stop the container</h4>
docker stop webserver

<h4>remove the container</h4>
docker rm webserver<

<h1>4. Attach Shell</h1>
docker run -it nginx -- /bin/bash
docker run -it --microsoft/powershell:nanoserver pwsh.exe
docker container exec -it [containername] -- bash

<h1>5. Cleaning Up</h1>
docker rm [containerName]
docker rm $(docker ps -a -q) (remove all the stopped containers)
docker images
docker rmi [imageName]
docker system prune -a (removes all the images that not in use by any containers).

<h1>6. Building</h1>
<h3>Builds an image using a DockerFile located in the same folder</h3>
docker build -t [name:tag] .
<h3>Builds an image using a Dockerfile located in the same folder</h3>
docker build -t [name:tag] -f [fileName]
<h3>Tag an existing image</h3>
docker tag [imageName] [name:tag] (tag is version)

--
Docker file
--
static html site

--
Docker tag
--
creates a target image<br>
myimage:v1<br>
repository default docker hub 
 
---
Persisting data
---
 1. Containers are ephemerous(short-lived) and stateless.
     we don't usually stores data in containers.
     Non-persistent data
    locally on writable layer
    it's the default, just write to the file system.
    when containers are destroyed,  so the data inside them

    **Persistent data**
    Stored outsied the container in a Volume.
    A volume is mapped to a logical folder.

---
Volumes
--
1. Create a new volume - docker create volume [volumeName]
2. Lists the volume - docker volume ls
3. Display the volume info - docker volume inspect [volumeName]
4. Deletes a volume - docker volume rm [volumeName]
5. Deletes all volumes not mounted - docker volume prune

--
mapping a volume
--
# create a volume<br>
docker volume create myvol

# inspect the volume<br>
docker volume inspect myvol

# list the volumes<br>
docker volume ls

# run a container with a volume 
docker run -d --name devtest{container}  -v d:/test/app nginx:latest

# to create a file in the volume using nano
docker exec -it voltesh bash 
apt-get update
apt-get install nano
cd app
nano test.txt

# Docker Compose
YAML
--
YAML ain't a markup language
Human friendly data serialization standard
Used by Docker-Compose and Kuberenetes.

 - Define and Run  mulitple containers applications
 - Define using yaml
 - run using the docker cli with compose plugin
 - compose specs
 
 Compose v1 cli is different from the docker cli and need python to installed
 Compose v2 
 apt-get install docker component
 
--
Docke compose cheat sheet
--
docker compose build = build the images
docker compose start = start the containers
docker compose stop = stop the container
docker compose up -d = build and start
docker compose ps
docker compose rm
docker compose down
docker compose logs
docker composer exec [container] bash.

docker compose --project-name test1 up -d
docker compose -p test2 up -d
Copy files from the container 
docker compose cp [containerId]:[src_path] [dest_path]
Copy files to the container
docker compose cp [src_path] [containerId]:[dest_path]


 
