# About Docker

- What is Docker:
  * Imagine you're developing an application, and it relies on specific packages to function properly. Once your development work is complete, you want to share the application with others for testing or usage. However, the recipients would typically need to configure their systems and install the necessary dependencies to match what you've set up on your system.
  * This is where Docker comes in handy. Docker simplifies the process by allowing you to package all the required dependencies of your application into container images. These images can be easily shared and executed on various platforms without the need for others to repetitively configure their systems or install dependencies from scratch.
    
- Architecture of Docker:
  
  ![docker_architecture](https://github.com/AnjaliPPrajapati/DockerLearning/assets/134782477/578e6a7a-c952-4085-847c-5e5c6f1197a6)
  
  * Docker Client: Docker clien is used to interact through Command line using the commands like docker pull, dcoker images, docker run etc. Docker client sends the request to docker daemon.
    
  * Docker Host: Docker Host contains Docker daemon, Docker Images and Docker Containers. The Docker daemon receives requests from the Docker Client and performs the requested actions. For example, when a "Docker Pull" request is made, the Docker daemon checks if the requested image is present; if it is, it delivers it to the Docker Client. If the image is not present, the Docker daemon fetches it from the Docker Registry and then returns it to the Docker Client.
    
  * Docker Registry: There are two types of Docker Registry. One is Private Registry and another is Public Registry also known as Docker Hub. Registry Conatins the Images, Extentions and Plugins. From here Docker Host pulls the image.
    
- What is Docker Image:
  * Docker image is a collection of code, libraries and all the dependencies that are required to run a software or an application. It can be defined as a blueprint of your application code.
  * Docker images are of two types: 1) Base image(Pre-build images) 2) Custom images
  * Base images are the images that already exist. For example Python image, Ngnix Image etc.
  * Custom images are the images that you create according to need of your application.
  * Custom Images can use multiple base images.
    
- What is container:
  * Container is a runtime environment for the Image. For instance, when you've pulled an image and you run it, the space where that Python image is up and running is what we call a container.
  * An isolated environent where te image is up and running along with it's dependencies is said to be as container.
    
- What is DockerFile:
  * DockerFike is a set of instructions that are required in order to run the application.
    
- What is Docker Compose:
  * Suppose you have an application which needs multiple different base images or custom images (which are built from Dockerfile), then in that case you would need to build image_1 from DockerFile_1 , image_2 from DockerFile_2 and so on. This obviously requires time to build each image individually and then up all the containers by running these images one by one.
  * So, by using Docker-compose, we can build and up all the containers at once just by giving one command "docker-compose up" .
