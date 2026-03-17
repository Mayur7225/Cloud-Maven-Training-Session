# 🚀 Docker Day 3 - Volumes & Networking

## 📌 Overview

In Day 3, I explored Docker Volumes and Docker Networking concepts.
This includes data persistence, volume types, and communication between containers.

---

## 📦 Docker Volumes

### 🔹 What are Docker Volumes?

Docker volumes are used to store data outside the container so that data is not lost when the container is removed.

### 🔹 Why use Volumes?

* Data persistence
* Safe storage outside container
* Useful for databases, logs, configs

---

## 🔹 Practical Implementation

### ✅ Step 1: Create Volume

```bash
docker volume create myvolume
```

### ✅ Step 2: Inspect Volume

```bash
docker volume inspect myvolume
```

---

### ✅ Step 3: Run Container with Volume

```bash
docker run -itd --name cont1 -v myvolume:/app ubuntu
```

---

### ✅ Step 4: Create File inside Container

```bash
docker exec -it cont1 /bin/bash
cd /app
touch file1.txt
```

---

### ✅ Step 5: Verify Persistence

```bash
docker rm -f cont1

docker run -itd --name cont2 -v myvolume:/app ubuntu
docker exec -it cont2 /bin/bash
cd /app
ls
```

✔️ Output:

```
file1.txt
```

👉 Data is persistent even after container deletion.

---

## ⚠️ Issue Faced

* Volume name mismatch (`myvolume` vs `myVolume`)
* Docker created a new volume due to case sensitivity

### ✅ Solution

* Used consistent naming: `myvolume`

---

## 🔗 Bind Mount

### 🔹 Command:

```bash
docker run -itd --name cont3 -v $(pwd):/app ubuntu
```

### 🔹 Use Case:

* Sync files between host and container
* Useful for development

---

## 🌐 Docker Networking

### 🔹 Create Network

```bash
docker network create my-network
```

---

### 🔹 Run Containers on Same Network

```bash
docker run -dit --name c1 --network my-network nginx
docker run -dit --name c2 --network my-network nginx
```

---

### 🔹 Test Communication

```bash
docker exec -it c1 /bin/bash
curl http://c2
```

✔️ Containers communicate successfully.

---

## 📚 Concepts Covered

* Docker Volumes

  * Named Volumes
  * Bind Mounts
* Data Persistence
* Docker Networking

  * Bridge Network
  * Container Communication

---

## 🧠 Key Learnings

* Volumes store data outside containers
* Data remains even after container deletion
* Volume names are case-sensitive
* Containers in same network can communicate using names

---

## 🛠 Commands Used

```bash
docker volume create
docker volume inspect
docker run -v
docker exec
docker network create
docker network ls
curl
```

---

## 📌 Conclusion

Docker volumes help manage persistent data efficiently, and Docker networking enables seamless communication between containers, which is essential for microservices architecture.

---

