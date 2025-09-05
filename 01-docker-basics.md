# Chapter 1: What is Docker? Why do we need it?

## 1.1 What is Docker?

Docker is a **containerization platform**.  
It allows developers to package an application together with all its dependencies (libraries, runtime, system tools, configs) into a single **unit called a container**.

- Containers are **lightweight**, **portable**, and run consistently across different environments.
- Unlike Virtual Machines, containers share the **host OS kernel**, making them faster and more efficient.

---

## 1.2 Why do we need Docker?

### The "It works on my machine" problem
- Developers often face issues where an app runs on their system but fails on servers or other machines.
- This happens because of differences in dependencies, OS, or configuration.

**Solution → Docker**  
With containers, the entire environment is bundled and shipped with the application, ensuring it runs identically everywhere.

---

## 1.3 Benefits of Docker

| Benefit | Explanation |
|---------|-------------|
| **Portability** | A container runs the same on any machine (local, server, cloud). |
| **Isolation** | Each container has its own environment → no conflicts. |
| **Consistency** | Same setup for dev, test, and production. |
| **Efficiency** | Containers are lightweight compared to Virtual Machines. |
| **Scalability** | Easy to scale apps by running multiple containers. |
| **Speed** | Containers start in seconds, unlike VMs which take minutes. |

---

## 1.4 Example: Without vs With Docker

### Without Docker
- Developer installs Node.js, libraries, dependencies manually.  
- Works on their system, but fails on production due to version mismatch.

### With Docker
- Package the Node.js app + dependencies into a container image.  
- The same container runs **anywhere** without setup issues.

---

## 1.5 Quick Demo Command

Run the official hello-world container:

```bash
docker run hello-world
````

* Docker CLI asks the **Docker Daemon** to run a container.
* If the `hello-world` image is not found locally, it is pulled from **Docker Hub**.
* A new container is created and executed, printing a test message.

---

## 1.6 Key Takeaways

* Docker solves the problem of **portability, consistency, and isolation**.
* Containers are **lightweight** compared to Virtual Machines.
* With Docker, apps run **the same everywhere**.

---

```
