# Day 6 – Terraform Basics, Jenkins & Docker Registry

## Topics Covered

### Terraform Basics

Learned the fundamentals of **Terraform** and Infrastructure as Code (IaC).

Key concepts covered:

* Infrastructure as Code (IaC)
* Terraform as an infrastructure provisioning tool
* Terraform configuration files
* Terraform workflow
* Terraform providers and resources
* `terraform init`
* `terraform validate`
* `terraform plan`
* `terraform apply`
* `terraform destroy`

### Terraform Workflow

```text
Terraform Configuration
        ↓
terraform init
        ↓
terraform validate
        ↓
terraform plan
        ↓
Check planned changes
        ↓
terraform apply
        ↓
Infrastructure Created
```

`terraform destroy` can be used when the created infrastructure needs to be removed.

---

# Hands-on DevOps Task

## Goal

Take an existing application and practice a basic **DevOps workflow** using:

**Git → GitHub → Docker → GHCR → Jenkins**

The task focused on understanding how an application moves from source code to a Dockerized application and how the Docker image can be stored and deployed using a container registry.

## Workflow

```text
Existing Application
        ↓
       Git
        ↓
     GitHub
        ↓
   Docker Image
        ↓
       GHCR
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

## Git & GitHub

Practiced the basic Git workflow:

```bash
git status
git add .
git commit -m "message"
git push
```

Used GitHub to store and manage the application source code.

## Docker

Worked with the application's Docker image and container.

Important Docker concepts practiced:

* Dockerfile
* Docker image
* Docker container
* Port mapping
* Docker commands
* Container lifecycle

## GitHub Container Registry (GHCR)

Pushed the Docker image to **GitHub Container Registry**.

### 1. Create GitHub Personal Access Token

Created a GitHub Personal Access Token for authentication with GHCR.

### 2. Login to GHCR

```bash
docker login ghcr.io
```

### 3. Tag the Docker Image

```bash
docker tag <image-name> ghcr.io/<username>/<image-name>:latest
```

### 4. Push the Image

```bash
docker push ghcr.io/<username>/<image-name>:latest
```

The Docker image was successfully stored in GHCR.

### 5. Pull the Image

```bash
docker pull ghcr.io/<username>/<image-name>:latest
```

### 6. Run the Container

```bash
docker run -d -p 8081:80 ghcr.io/<username>/<image-name>:latest
```

The image was pulled from GHCR and used to create a Docker container.

### 7. Verify the Container

```bash
docker ps
```

The application was successfully running inside the Docker container.

---

# Jenkins

Also explored the **Jenkins UI** and learned the basics of Jenkins as a CI/CD automation tool.

Covered:

* Jenkins dashboard
* Jenkins UI
* Jobs and pipelines
* Basic Jenkins concepts
* Role of Jenkins in DevOps

The overall workflow helped me understand how these tools work together in a DevOps environment.

## Tools Used

* Git
* GitHub
* Docker
* GitHub Container Registry (GHCR)
* Jenkins
* Terraform

## Key Learning

This practice helped me understand the connection between **source code management, containerization, container registries, automation, and infrastructure provisioning**.

The main DevOps flow practiced was:

```text
Git → GitHub → Docker → GHCR → Docker Pull → Docker Container → Running Application
```

Along with this, I learned the fundamentals of **Terraform and Infrastructure as Code**, which is an important part of automating infrastructure in DevOps.
