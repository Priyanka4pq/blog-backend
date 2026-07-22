# Blog Backend — DevOps CI/CD Pipeline

A RESTful API backend for a full-stack MERN blog application, built with **Node.js, Express.js, and MongoDB**, and deployed through a complete production-style CI/CD pipeline.

This repo is the **backend + DevOps pipeline** half of a three-tier blog application. The frontend lives in a separate repo: [blog-Frontend](https://github.com/Priyanka4pq/blog-Frontend).

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)

## 🚀 Live Demo
**Backend URL:** [https://priblogback.vercel.app](https://priblogback.vercel.app)

## 🏗️ Architecture — Three-Tier Deployment

```
Presentation Tier  →  blog-Frontend (React)
Application Tier   →  This repo (Node.js / Express)
Data Tier          →  MongoDB
```

## 🔄 CI/CD Pipeline

```
Code pushed to GitHub
        ↓
Jenkins pipeline triggers automatically
        ↓
Source code built & analyzed with SonarQube (static code analysis)
        ↓
Docker image built & pushed to Docker Hub
        ↓
Kubernetes (kubeadm) deploys the latest image
        ↓
Prometheus scrapes application & cluster metrics
        ↓
Grafana dashboards visualize metrics in real time
```

## ✨ Features
- RESTful API for Blog operations (CRUD)
- User Authentication & Authorization
- Middleware for error handling and validation
- MongoDB integration with Mongoose
- Secure environment configuration
- Fully containerized with Docker
- Kubernetes-ready deployment manifests
- End-to-end CI/CD with Jenkins
- Static code analysis via SonarQube on every build
- Live monitoring via Prometheus + Grafana

## 🛠️ Tech Stack
| Layer | Tools |
|---|---|
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (Mongoose ODM) |
| **CI/CD** | Jenkins |
| **Code Quality** | SonarQube |
| **Containerization** | Docker, Docker Hub |
| **Orchestration** | Kubernetes (kubeadm) |
| **Monitoring** | Prometheus, Grafana |
| **Deployment** | Vercel (live demo), Kubernetes (cluster deployment) |

## 📁 Project Structure
```
blog-backend/
├── src/
│   ├── data/         # Sample data
│   ├── middleware/   # Auth, error handling, etc.
│   ├── model/        # Mongoose models
│   └── routers/      # API routes
├── Jenkins/           # Jenkinsfile & pipeline scripts
├── Manifests/          # Kubernetes YAML files
├── Dockerfile
├── index.js
├── package.json
└── vercel.json
```

## 🏃 How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/Priyanka4pq/Blog-Backend-DevOps-Pipeline.git
   cd Blog-Backend-DevOps-Pipeline
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file and add your MongoDB connection string.
4. Run the server:
   ```bash
   npm start
   ```

## 🐳 Docker
```bash
# Build image
docker build -t blog-backend .

# Run container
docker run -p 5000:5000 blog-backend
```

## ☸️ Kubernetes
Deployment manifests are in the `/Manifests` folder. Deploy with:
```bash
kubectl apply -f Manifests/
```

## 🔧 CI/CD Pipeline Details
The `Jenkinsfile` in `/Jenkins` defines the following stages:
1. **Checkout** — pulls latest code from GitHub
2. **Code Analysis** — runs SonarQube static analysis and quality gate check
3. **Build** — builds the Docker image
4. **Push** — pushes the image to Docker Hub
5. **Deploy** — applies Kubernetes manifests to the cluster
6. **Monitor** — Prometheus scrapes app/cluster metrics; Grafana dashboards visualize them

## 📌 Future Enhancements
- JWT Authentication
- Blog image upload (Cloudinary/AWS S3)
- Advanced search & pagination
- Helm chart for simplified deployment

---
**Made with ❤️ by Priyanka**
