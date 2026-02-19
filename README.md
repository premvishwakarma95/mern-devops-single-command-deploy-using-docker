# MERN Monorepo – Single Command DevOps Deployment

This repository demonstrates a **production-style MERN stack application** deployed using **Docker, Docker Compose, Nginx, and SSL (Certbot)** — all runnable with **a single command**.

The goal of this project is to show how a full-stack MERN application can be **containerized, orchestrated, and deployed** on a Linux server (e.g. AWS EC2) using DevOps best practices.

---

## 🚀 What This Repository Does

- Runs **Frontend (React)** and **Backend (Node.js / Express)** in a **single monorepo**
- Uses **Docker** to containerize all services
- Uses **Docker Compose** to start everything together
- Uses **Nginx** as a reverse proxy
- Uses **MongoDB** as the database (containerized)
- Uses **Certbot** to generate and manage SSL certificates
- Allows the entire application stack to be started with **one command**

---

## 🧱 Tech Stack

- **Frontend:** React
- **Backend:** Node.js, Express
- **Database:** MongoDB
- **Reverse Proxy:** Nginx
- **Containerization:** Docker
- **Orchestration:** Docker Compose
- **SSL:** Certbot (Let’s Encrypt)
- **OS:** Linux (Ubuntu / Amazon Linux)

---

## 📁 Project Structure
.
├── backend/ # Node.js + Express backend
├── frontend/ # React frontend
├── nginx/ # Nginx config and entrypoint
├── certbot/ # SSL certificate automation scripts
├── docker-compose.yml # Orchestrates all services
├── install-docker.sh # Installs Docker & Docker Compose
├── .env.example # Environment variable template
└── README.md
```yaml

---

## 🧠 Architecture Overview

```
Client (Browser)
|
v
Nginx (80 / 443)
|
|----> Frontend (React)
|
|----> Backend (Node.js / Express)
|
v
MongoDB
```yaml

- **Nginx** serves the frontend and proxies API requests
- **Backend** handles APIs and business logic
- **MongoDB** stores application data
- **Certbot** manages HTTPS certificates

---

## ⚙️ Prerequisites

- Linux server (AWS EC2 recommended)
- Git installed
- Public IP or domain name (for SSL)

---

## 🛠️ Setup & Deployment (Single Command)

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2️⃣ Install Docker & Docker Compose

```bash
chmod +x install-docker.sh
./install-docker.sh
```

3️⃣ Configure Environment Variables
```bash
cp .env.example .env
```
Update values inside .env (ports, domain, DB URL, etc.).

4️⃣ Start the Entire Stack 🚀
```bash
docker compose up -d
```
✅ Frontend
✅ Backend
✅ MongoDB
✅ Nginx
✅ SSL

All running with one command.
