# Day 5 – Jenkins & GitHub Container Registry

## Topics Covered

* Introduction to Jenkins
* Jenkins UI and basic components
* Understanding Jenkins workflow
* GitHub Container Registry (GHCR)
* Docker image tagging and pushing
* Docker image pulling and running containers
* GitHub Personal Access Token (PAT)

## Hands-on Task

In this task, I worked with a Dockerized application and pushed its Docker image to **GitHub Container Registry (GHCR)**.

### Workflow

```text
Application
    ↓
Docker Image
    ↓
GitHub Container Registry (GHCR)
    ↓
Docker Pull
    ↓
Docker Image
    ↓
Docker Run
    ↓
Docker Container
    ↓
Application Running
```

## Commands Practiced

### 1. Create GitHub Personal Access Token

A GitHub Personal Access Token was created to authenticate Docker with GHCR.

### 2. Login to GHCR

```bash
docker login ghcr.io
```

### 3. Tag the Docker Image

```bash
docker tag <local-image> ghcr.io/<github-username>/<image-name>:latest
```

### 4. Push the Image to GHCR

```bash
docker push ghcr.io/<github-username>/<image-name>:latest
```

The Docker image is now available in the GitHub Container Registry.

### 5. Pull the Image from GHCR

```bash
docker pull ghcr.io/<github-username>/<image-name>:latest
```

### 6. Run the Container

```bash
docker run -d -p 8081:80 ghcr.io/<github-username>/<image-name>:latest
```

### 7. Verify the Running Container

```bash
docker ps
```

The container starts successfully and the application can be accessed through the mapped port.

## Key Learning

This task helped me understand how a Docker image can be **built, tagged, pushed to GHCR, pulled from the registry, and deployed as a running Docker container**.

It also gave me a basic understanding of how **Jenkins, Docker, GitHub, and container registries** fit into a DevOps workflow.

## Tools Used

* Jenkins
* Docker
* GitHub
* GitHub Container Registry (GHCR)
* Git Bash / PowerShell
