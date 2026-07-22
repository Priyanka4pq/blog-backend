```markdown
# Blog Backend

A robust RESTful API backend for a Blog application built with **Node.js, Express.js, and MongoDB**. Fully containerized and integrated with modern DevOps practices.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

## 🚀 Live Demo
**Backend URL:** [https://priblogback.vercel.app](https://priblogback.vercel.app)

## ✨ Features
- RESTful API for Blog operations (CRUD)
- User Authentication & Authorization
- Middleware for error handling and validation
- MongoDB integration with Mongoose
- Secure environment configuration
- Containerized with Docker
- Ready for Kubernetes deployment
- CI/CD ready with Jenkins

## 🛠️ Tech Stack
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (Mongoose ODM)
- **DevOps:**
  - Docker
  - Kubernetes (Manifests included)
  - Jenkins CI/CD
  - Vercel Deployment

## 📁 Project Structure
```
blog-backend/
├── src/
│   ├── data/           # Sample data
│   ├── middleware/     # Auth, error handling, etc.
│   ├── model/          # Mongoose models
│   └── routers/        # API routes
├── Jenkins/            # Jenkins pipeline scripts
├── Manifests/          # Kubernetes YAML files
├── Dockerfile
├── index.js
├── package.json
└── vercel.json
```

## 🏃‍♀️ How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/Priyanka4pq/blog-backend.git
   cd blog-backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create `.env` file and add your MongoDB connection string.

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
Kubernetes manifests are available in the `/Manifests` folder.

## 📌 Future Enhancements
- JWT Authentication
- Blog image upload (Cloudinary/AWS S3)
- Frontend integration (React)
- Advanced search & pagination

---

**Made with ❤️ by Priyanka**
