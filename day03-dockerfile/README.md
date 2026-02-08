# Day 3 — Dockerfile Practical

On Day 3 of my DevOps learning journey, I learned how to build my own Docker image using a Dockerfile instead of only running prebuilt images. This helped me understand how applications are packaged and deployed in real-world DevOps workflows.

## Goal
Create a custom Docker image using nginx and serve my own HTML page inside a container.

## Files Used
- Dockerfile: Defines how the Docker image is built  
- index.html: Custom HTML page served by nginx  

## Steps Performed

### 1. Created a simple HTML page
I created an index.html file that displays a custom message for Day 3.

### 2. Created a Dockerfile
The Dockerfile uses nginx as the base image and replaces the default nginx page with my custom HTML file.

Dockerfile content:
FROM nginx:latest  
COPY index.html /usr/share/nginx/html/index.html  

### 3. Built the Docker image
I built a custom Docker image locally using the following command:

docker build -t surabhi-day3-nginx .

### 4. Ran the container with port mapping
I ran the container and mapped a local port to the container’s port so it could be accessed in the browser:

docker run -d -p 8082:80 surabhi-day3-nginx

This maps port 8082 on my laptop to port 80 inside the container.

### 5. Verified in the browser
I opened the browser and accessed:

http://localhost:8082

The custom HTML page loaded successfully, confirming that the Docker image and container were working correctly.

## Outcome
- Learned how to write and use a Dockerfile  
- Built a custom Docker image  
- Ran a container using my own image  
- Understood how applications are packaged and served using Docker
