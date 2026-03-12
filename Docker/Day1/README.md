# Docker - Day 1 (Basics and Fundamental Commands)

## Introduction

Docker is a containerization platform that allows developers to package an application and its dependencies into a container. Containers ensure that the application runs consistently across different environments such as development, testing, and production.

For example, if an application works on a developer's laptop, Docker ensures it will run the same way on a server.

---

## Project Structure

```
cloude-maven/
│
├── docker/
│   └── README.md
│
└── pom.xml
```

### Explanation

- **cloude-maven/** – Main project repository  
- **docker/** – Folder created for Docker learning and documentation  
- **README.md** – Documentation for Docker Day 1 commands and concepts  
- **pom.xml** – Maven configuration file for the Java application

---

## Basic Docker Commands

### 1. Check Docker Version

```
docker --version
```

**Purpose**

Displays the installed Docker version on the system.

**Use Case**

Used to verify that Docker is installed correctly on the machine.

---

### 2. Display Docker System Information

```
docker info
```

**Purpose**

Shows detailed information about Docker including number of containers, images, storage drivers, and system configuration.

**Use Case**

Helpful for understanding the Docker environment and troubleshooting issues.

---

### 3. Pull an Image from Docker Hub

```
docker pull nginx
```

**Purpose**

Downloads the nginx image from Docker Hub to the local system.

**Use Case**

Used when you want to run a prebuilt application such as a web server or database.

---

### 4. List Docker Images

```
docker images
```

**Purpose**

Displays all Docker images available on the local system.

**Use Case**

Used to check which images are already downloaded.

---

### 5. Run a Docker Container

```
docker run nginx
```

**Purpose**

Creates and starts a container from the nginx image.

**Use Case**

Used to run an application inside a container.

---

### 6. Run Container in Detached Mode

```
docker run -d nginx
```

**Purpose**

Runs the container in the background.

**Use Case**

Used in production environments where services need to run continuously.

---

### 7. List Running Containers

```
docker ps
```

**Purpose**

Displays all currently running containers.

**Use Case**

Helps monitor active services running in Docker.

---

### 8. List All Containers

```
docker ps -a
```

**Purpose**

Displays all containers including running and stopped containers.

**Use Case**

Useful for troubleshooting containers that have stopped.

---

### 9. Stop a Running Container

```
docker stop container_id
```

**Purpose**

Stops a running container.

**Use Case**

Used when a running service needs to be stopped temporarily.

---

### 10. Remove a Container

```
docker rm container_id
```

**Purpose**

Deletes a stopped container from the system.

**Use Case**

Used to clean up unused containers.

---

### 11. Remove a Docker Image

```
docker rmi image_id
```

**Purpose**

Deletes a Docker image from the local system.

**Use Case**

Used to free disk space or remove unused images.

---

## Docker Key Concepts

### Image
A Docker image is a template used to create containers.

Example:
- nginx
- ubuntu
- mysql

### Container
A container is a running instance of a Docker image.

### Docker Hub
Docker Hub is a public registry where Docker images are stored and shared.

---

## Summary

On Day 1, we learned the fundamentals of Docker including how to:

- Verify Docker installation
- Pull images from Docker Hub
- Run containers
- Manage containers and images
- Understand basic Docker concepts
