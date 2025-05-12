# Elevate-Labs-project

# Node.js CI/CD Pipeline with Docker

This project demonstrates a CI/CD pipeline for a Node.js application using GitHub Actions and DockerHub. The pipeline automates the following steps:

1. **Build the application**
2. **Run tests**
3. **Dockerize the application**
4. **Push Docker image to DockerHub**

## 🚀 Project Structure

```
nodejs-demo-app/
│
├── app.js              # Main application file
├── Dockerfile          # Docker configuration
├── package.json        # Node.js dependencies
├── package-lock.json   # Dependency lock file
└── .github/
    └── workflows/
        └── main.yml   # GitHub Actions workflow
```

---

## 🛠️ Prerequisites

* Node.js (v18 or higher)
* npm (v9 or higher)
* Docker
* Git

---

## 📦 Setup Instructions

```bash
# Clone the repository
git clone https://github.com/vishwajeet937/Elevate-Labs-project.git

# Navigate into the project directory
cd nodejs-demo-app

# Install dependencies
npm install

# Run the application
node app.js

# Visit http://localhost:3000 to see the app running
```

---

## 🐳 Docker Setup

```bash
# Build the Docker image
docker build -t your-dockerhub-username/nodejs-demo-app .

# Run the Docker container
docker run -p 3000:3000 your-dockerhub-username/nodejs-demo-app

# Visit http://localhost:3000 to see the app running in Docker
```

---

## 🔄 CI/CD Pipeline

The CI/CD pipeline is managed using **GitHub Actions**. It is triggered on a `push` to the `main` branch.

**Pipeline Steps:**

1. Checkout code
2. Install dependencies
3. Run tests
4. Build Docker image
5. Push Docker image to DockerHub

### GitHub Secrets:

* `DOCKER_USERNAME`: Your DockerHub username
* `DOCKER_PASSWORD`: Your DockerHub password

---

## 👀 Monitoring Logs

To view application logs:

```bash
docker logs <container_id>
```

To view GitHub Action logs, go to the **Actions** tab in your GitHub repository.

---

## 🌐 Deployment

The Docker image can be pulled and run from DockerHub:

```bash
docker pull your-dockerhub-username/nodejs-demo-app

docker run -p 3000:3000 your-dockerhub-username/nodejs-demo-app
```

Access the application at `http://localhost:3000`

---

## 🤝 Contributing

Feel free to fork this repository, open issues, and submit pull requests.

---

## 📜 License

MIT License

---

**Developed by Vishwajeet Kumar**
