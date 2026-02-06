# Day 2 — Docker Practical 🐳

Today I did my first Docker practical and proved it by running nginx in a container.

## What I did (step by step)
1. Checked Docker is installed
2. Pulled the nginx image
3. Ran nginx in foreground and stopped it
4. Ran nginx in background
5. Mapped ports so I can open nginx in the browser
6. Verified it on http://localhost:8080
7. Stopped and removed the container (cleanup)

## Commands I used
```bash
docker --version
docker pull nginx
docker run nginx
# (stop with CTRL + C)
docker run -d nginx
docker ps
docker stop <container_id>
docker run -d -p 8080:80 nginx
docker ps
docker stop <container_id>
docker rm <container_id>

Browser proof

I opened:http://localhost:8080 and saw the nginx welcome page.

![Nginx Welcome Page](screenshots/nginx-welcome.png)
