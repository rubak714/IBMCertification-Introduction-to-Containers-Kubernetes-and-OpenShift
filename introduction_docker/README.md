## 🔗 Introduction to Docker 

### 🔗 What is Docker?

**Docker** is a popular open-source platform that enables developers to build, run, and manage applications in lightweight, portable units called **containers**.

> Although container technology existed before Docker, the launch of Docker in 2013 made containers accessible and easy to use.

Docker has become synonymous with containerization due to its simplicity, community support, and strong ecosystem.

---

### 🔗 Docker as a Toolset

Docker provides:

* A **platform** to build and run containers
* A **command-line interface (CLI)** for creating, managing, and deploying container images
* A **runtime engine** to execute containers

---

### 🔗 Docker Components

| Concept          | Description                                                                   |
| ---------------- | ----------------------------------------------------------------------------- |
| Docker Image     | A blueprint for creating a container, defined using a `Dockerfile`            |
| Docker Container | A running instance of a Docker image, isolated and portable                   |
| Docker CLI       | Command-line tool to build, run, and manage containers (`docker build`, etc.) |
| Docker Daemon    | The background process that manages containers and images                     |

---

### 🔗 Common Docker CLI Commands

* `docker build` – Builds a container image from a Dockerfile
* `docker tag` – Tags (renames) an image
* `docker images` – Lists available images on your machine
* `docker run` – Launches a new container from an image
* `docker push` – Uploads an image to a remote container registry
* `docker pull` – Downloads an image from a container registry

> You'll use all these commands hands-on in course labs.

---

### 🔗 Docker in the Architecture Stack

```
| Applications     |
|------------------|
| Container Runtime|  <-- Docker or containerd
| Operating System |
| Hardware         |
```

* Docker acts as the **container runtime**, sitting between your OS and the containerized applications.

---

### 🔗 Docker and Other Runtimes

* **containerd**: A container runtime introduced by Docker, now widely adopted
* **rkt**: An alternative container runtime
* Docker uses **containerd** under the hood in modern setups

---

### 🔗 Summary

* Docker simplifies working with containers
* It provides tooling to build, run, and manage containers
* It's part of a larger container ecosystem, essential in DevOps and cloud-native workflows
