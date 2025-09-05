# Chapter 2: Docker Images & Containers

## 2.1 What is a Docker Image?

- A **Docker Image** is a **blueprint** (read-only template) used to create containers.
- Images include:
  - Application code
  - Runtime (e.g., Node.js, Python, Java)
  - Libraries & dependencies
  - Environment variables & configurations

📌 Example:  
- `ubuntu:20.04` → Ubuntu OS image  
- `node:18-alpine` → Node.js image (based on Alpine Linux)  

You can pull an image from Docker Hub:

```bash
docker pull ubuntu:20.04
````

---

## 2.2 What is a Docker Container?

* A **Docker Container** is a **running instance of an image**.
* Containers are **isolated environments** with:

  * Their own filesystem
  * Own processes
  * Own network stack
* They are lightweight because they share the host OS kernel.

📌 Example: Running an Ubuntu container:

```bash
docker run -it ubuntu:20.04 bash
```

This command:

1. Pulls the Ubuntu image (if not already available).
2. Creates a container from it.
3. Attaches an interactive terminal (`-it`) with `bash`.

---

## 2.3 Relationship Between Images & Containers

* **Image = Blueprint** (recipe)
* **Container = Instance** (prepared dish)

📌 Analogy:

* **Image** = a class in programming
* **Container** = an object created from that class

---

## 2.4 Lifecycle of Containers

1. **Create** → `docker create IMAGE`
2. **Start** → `docker start CONTAINER_ID`
3. **Run (create + start)** → `docker run IMAGE`
4. **Stop** → `docker stop CONTAINER_ID`
5. **Remove** → `docker rm CONTAINER_ID`

List containers:

```bash
docker ps        # running containers
docker ps -a     # all containers (including stopped)
```

---

## 2.5 Example Workflow

```bash
# Pull an image
docker pull alpine

# Run a container
docker run alpine echo "Hello Docker!"

# List containers
docker ps -a

# Remove a container
docker rm <container_id>
```

---

## 2.6 Key Takeaways

* **Image** = read-only template.
* **Container** = running instance of an image.
* One image can spawn **multiple containers**.
* Images live in registries (like Docker Hub), containers live on your host machine.

---
