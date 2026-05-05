# 🐳 Docker Container Running Nginx Web Server

A beginner-friendly project demonstrating how to containerize a static web page using **Docker** and **Nginx**.

## 📋 Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and **running**
- A terminal (PowerShell, CMD, or bash)

## 🗂️ Project Structure

```
Docker-container-running-NGINX/
├── Dockerfile
└── index.html
```

## ⚙️ Setup & Usage

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/docker-nginx-app.git
cd docker-nginx-app
```

### 2. Build the Docker image

```bash
docker build -t my-nginx-app .
```

### 3. Run the container

```bash
docker run -d -p 8080:80 my-nginx-app
```

### 4. Open in browser

Navigate to: [http://localhost:8080](http://localhost:8080)

## 🐋 Dockerfile Explained

```dockerfile
FROM nginx:alpine      # Use lightweight Nginx base image
COPY ./index.html /usr/share/nginx/html   # Copy our HTML into the container
EXPOSE 80              # Expose port 80 (Nginx default)
```

## 🛠️ Common Issues

| Error | Cause | Fix |
|-------|-------|-----|
| `failed to connect to docker API` | Docker Desktop not running | Open Docker Desktop and wait for it to fully start |
| `requires 1 argument` | Missing `.` in build command | Use `docker build -t my-nginx-app .` (note the dot) |
| Page not loading | Container not running | Check with `docker ps` |

## 📦 Useful Docker Commands

```bash
# List running containers
docker ps

# Stop the container
docker stop <container_id>

# Remove the container
docker rm <container_id>

# Remove the image
docker rmi my-nginx-app
```

## 🧰 Technologies Used

- [Docker](https://www.docker.com/)
- [Nginx](https://nginx.org/) (Alpine variant)
- HTML / CSS

## 📄 License

MIT License — feel free to use and modify.
