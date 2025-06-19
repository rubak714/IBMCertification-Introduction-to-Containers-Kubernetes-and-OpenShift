## 🔗 Building Container Images with Docker

### 🔗 What is a Container Image?

A **container image** is a lightweight, standalone, and immutable file that contains all the code, dependencies, environment variables, and configurations needed to run an application. Think of it as a blueprint or template.

> A container is a **running instance** of that image, just like an object is an instance of a class in programming.

---

### 🔗 The Dockerfile: Blueprint for Images

To create a container image, you start with a **Dockerfile**—a simple text file with instructions on how to build the image.

Example:

```Dockerfile
FROM ubuntu:18.04
COPY ./app /app
RUN make /app
CMD ["python3", "/app/app.py"]
```

---

### 🔗 Image Layers Explained

Each instruction in a Dockerfile creates a **new read-only layer**. Docker stacks these layers to form the final image.

| Dockerfile Instruction | Description                                        |
| ---------------------- | -------------------------------------------------- |
| `FROM`                 | Specifies the base image (e.g., Ubuntu, Python)    |
| `COPY` or `ADD`        | Copies files into the image                        |
| `RUN`                  | Executes a shell command (e.g., install libraries) |
| `ENV`                  | Sets environment variables                         |
| `CMD`                  | Defines the default command for the container      |

> Layers are shared across images, saving disk space and improving performance.

---

### 🔗 From Dockerfile to Container

1. **Write** a Dockerfile
2. **Build** the image: `docker build -t myapp .`
3. **Run** the image as a container: `docker run myapp`

During execution, Docker adds a **writable layer** on top of the image layers so the container can operate.

---

### 🔗 Key Concepts

* **Images** are immutable and shareable across systems
* **Containers** are executable, with isolated writeable layers
* **Dockerfile** defines how images are built

---

### 🔗 Summary

* Images are constructed step-by-step using Dockerfile instructions
* They are versioned, layered, and optimized for reusability
* Containers are created from images and can be run anywhere

