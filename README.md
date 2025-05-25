# 🎵 JukeBox - Music Recommendation Web App

JukeBox is a full-stack music recommendation application that uses a Flask backend for AI-based song suggestions and a Node.js server to serve frontend APIs. This project is fully containerized using Docker Compose.

## 📦 Project Structure

```
jukebox/
├── jukebox-backend/
│   ├── recom_model/          # Flask backend (Python)
│   │   ├── Dockerfile
│   │   └── app.py
│   ├── Dockerfile            # Node.js server
│   └── server.js
├── docker-compose.yml
└── README.md
```

## 🚀 How to Run the Containers

### 1. Build the Images
From the project root, run:
```bash
docker compose build
```

### 2. Run the Containers
```bash
docker compose up
```

To run in background (detached mode):
```bash
docker compose up -d
```

## 🌐 Access the App

| Service         | URL                     |
|----------------|--------------------------|
| Node.js Server | http://localhost:3000    |
| Flask Backend  | http://localhost:5000    |

## ✅ Test the Student API Endpoint

Visit this URL in your browser or Postman:
```
http://localhost:5000/api/student
```

Expected JSON output:
```json
{
  "name": "Dhanush Soma",
  "student_id": "224967723"
}
```

## 🐳 Docker Compose Overview

This app uses Docker Compose to run two containers:
- `backend` (Flask server) on port `5000`
- `node-server` (Node.js API) on port `3000`

Inter-service communication is handled via Docker's internal networking. The `node-server` can call the Flask backend using the service name `backend`.

## 📘 Author

**Dhanush Soma**  
Master’s of IT (Professional) – Deakin University
