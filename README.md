# Cloud-First-Project-Docker

## Overview

This project is designed to introduce the concept of containerization, specifically utilizing the popular tool Docker. Through a series of tutorials and exercises, you will become familiar with Docker's key concepts and practical use cases. The following topics are covered:

- **Introduction to Docker**
- **Installing Docker**
- **Working with Docker CLI commands**
- **Docker Images and Containers**
- **Creating Dockerfiles**
- **Creating Docker Images**
- **Running Docker Containers**
- **Commands for Managing Images and Containers**
- **Understanding Web Servers**
- **Working with Postman**

In this project, you'll be provided with the necessary resources, commands, and Dockerfiles for various applications. Your tasks include writing Dockerfiles and creating Docker images for the following components:

- Docker file for the `ping-pong-java` application
- Docker file for the `ping-pong-python` application
- Docker file for the `ping-pong-js` application
- Docker file for `nginx`

## Docker Files

### Docker File for ping-pong-java Application

- **Endpoints**:
  - `/ping`: GET method to receive "ping" as a response
- **Port**: 8001
- **Command to Run**:
  ```bash
  javac PingPong.java
  java PingPong

- **Base Image: Use 8**:openjdk
- **Network Alias**: javaapp

### Docker File for ping-pong-python Application

- **Endpoints**:
  - /ping: GET method to receive "ping" as a response
  - /echo: POST method with "echo":"text" to receive "text" as a response
- **Port**: 8002
**Command to Run**:
  ```bash
  uvicorn PingPong:app --host 0.0.0.0 --port 8002 --reload
- **Base Image**: Use tiangolo/uvicorn-gunicorn-fastapi
- **Network Alias**: pythonapp

### Docker File for ping-pong-js Application

- **Endpoints**:
  - /ping: GET method to receive "ping" as a response
- **Port**: 8003
- **Command to Run**:
  ```bash
  node PingPong.js
- **Base Image**: Use node:slim
- **Network Alias**: jsapp

### Docker File for nginx
- **Configuration**: The provided config file acts as a reverse proxy for applications, hosts a static HTML page, and provides access to contents outside the container for download.
- **Path**: /etc/nginx/nginx.conf
### Network: 
- To make the container accessible to other containers, ensure they are in the same network.

### Screenshots

Check the "screenshot" folder for images of the output of each section.


I hope this Docker Cloud Project helps you gain a comprehensive understanding of Docker and its practical applications. Enjoy your containerization journey!

### Authors
Mehrnaz Sadeghieh
