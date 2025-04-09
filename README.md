

# 🧮 Advance Calculator Microservice

This project is a basic calculator microservice built using **Node.js** and **Express**. It supports **addition**, **subtraction**, **multiplication**, and **division** through REST API endpoints. It also includes **logging** using the Winston library and a **simple web UI**.

---

## 🛠️ Features

- REST API for basic arithmetic operations
- Input validation and error handling
- Logging with Winston (console and file logs)
- Minimal web UI for testing operations

---

## 📁 Project Structure
```
├── logs/ │ 
├── combined.log │
    └── error.log 
├── public/ │ 
    └── index.html 
├── docker-compose.yml
├── Dockerfile 
├── logger.js 
├── server.js 
├── package.json 
└── README.md
```

2. Install Dependencies by using - "npm install"

3. Run the Microservice by using - "node server.js"

4. Access it via: http://localhost:3003 


# 🐳 Dockerizing the Application
## 🔧 Prerequisites
- Git (https://github.com)
- Visual Studio code (https://code.visualstudio.com/)
- Node.js (https://nodejs.org/en/download/)
- Docker (https://app.docker.com/)


# 📦 Steps to Dockerize and Run the App
- bash
- Copy
- Edit

# 1. Clone the repository
git clone https://github.com/samarth9702/sit737-2025-prac5p.git
cd sit737-2025-prac5p

# 2. Build the Docker image
docker build -t sit737-prac5p-app .

# 3. Start using Docker Compose
docker-compose up

Now go to: http://localhost:3003

# ❤️ Docker Health Check + Auto Restart
This app includes a Docker health check and restart: always policy via docker-compose.yml:

```
Copy
Edit
healthcheck:
  test: ["CMD", "curl", "-f", "http://localhost:3003"]
  interval: 30s
  timeout: 10s
  retries: 3
restart: always
```
This ensures the container is monitored and will restart automatically if it becomes unhealthy.

# 🚀 Push to Docker Hub
```
# 1. Tag the image
docker tag calculator-app your_dockerhub_username/sit737-5.1

# 2. Login and push
docker login
docker push your_dockerhub_username/sit737-5.1
```