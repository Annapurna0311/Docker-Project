# What is Docker?
Docker is a platform designed to make it easier to develop, deploy, and run applications using containers. Containers allow developers to package an application along with all its dependencies, libraries, and configuration files into a single standardized unit. This makes the app portable and consistent across different environments, ensuring it runs the same way regardless of where it’s deployed (on a developer’s machine, a testing environment, or a production server).

Key Concepts:
* Image: A lightweight, stand-alone, executable package that includes everything needed to run a piece of software (code, runtime, libraries, environment variables, and configuration files).
* Container: A running instance of a Docker image. It is isolated from other containers and the host system.
* Dockerfile: A script that contains a series of instructions on how to build a Docker image.
* Docker Hub: A cloud-based registry where Docker images are stored, and users can pull or push their images.

  Common Docker Commands
1. docker build
    Purpose: Builds a Docker image from a Dockerfile.
    Syntax: docker build -t <image-name> .
    Example:
    docker build -t myapp .
    This will build an image named myapp from the Dockerfile in the current directory.
2. docker run
    Purpose: Runs a container from an image.
    Syntax: docker run [options] <image-name>
    Example:
    docker run -it ubuntu
    This will run a container using the ubuntu image interactively.
   
    Options:
    -d: Run container in detached mode (in the background).
    -p: Publish container's port to the host.
    --name: Assign a name to the container.
    -v: Mount a volume.
4. docker ps
    Purpose: Lists running containers.
    Syntax: docker ps
    Example:
    docker ps
    This will list all the currently running containers.
    docker ps -a: Shows all containers (running or stopped).
5. docker pull
    Purpose: Pulls a Docker image from a registry like Docker Hub.
    Syntax: docker pull <image-name>
    Example:
    docker pull nginx
    This command pulls the nginx image from Docker Hub.
6. docker stop
    Purpose: Stops a running container.
    Syntax: docker stop <container-id>
    Example:
    docker stop myapp-container
    This will stop the container with the name myapp-container.
7. docker exec
    Purpose: Executes a command inside a running container.
    Syntax: docker exec -it <container-id> <command>
    Example:
    docker exec -it myapp-container /bin/bash
    This will open a Bash shell inside the myapp-container container.
8. docker rm
    Purpose: Removes a stopped container.
    Syntax: docker rm <container-id>
    Example:
    docker rm myapp-container
    This removes the container with the name myapp-container.
9. docker rmi
    Purpose: Removes an image.
    Syntax: docker rmi <image-id>
    Example:
    docker rmi myapp-image
    This removes the myapp-image from the local image store.
10. docker images
    Purpose: Lists all Docker images on the system.
    Syntax: docker images
    Example:
    docker images
    This lists all the images available on the local machine.
11. docker logs
    Purpose: Fetches the logs of a container.
    Syntax: docker logs <container-id>
    Example:
    docker logs myapp-container
    This command retrieves the logs from the container named myapp-container.

    
# Basic Docker Workflow
* Write a Dockerfile: Define the application environment and dependencies in a Dockerfile.
* Build the image: Use the docker build command to create an image from the Dockerfile.
* Run a container: Use the docker run command to start the image as a container.
* Push to Docker Hub (optional): Use docker push to upload your image to Docker Hub for sharing or deployment.
