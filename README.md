# 🚀 Task 2 — CI/CD Pipeline using Jenkins & Docker

## 📌 Project Overview

This project demonstrates a simple CI/CD pipeline for a Node.js application using Jenkins and Docker.

Jenkins is used to automate the process of getting the source code from GitHub, installing dependencies, testing the application, and building a Docker image.

## 🎯 Objective

The main objective of this task is to understand how Jenkins can automate a CI/CD pipeline.

The pipeline automatically performs the following steps:

Code → GitHub → Jenkins → Install Dependencies → Test → Build Docker Image

## 🛠️ Technologies Used

- Node.js
- Express.js
- Git & GitHub
- Jenkins
- Docker
- Docker Hub

## 🔄 CI/CD Workflow

Developer
    ↓
Push Code to GitHub
    ↓
GitHub Repository
    ↓
Jenkins
    ↓
Checkout Code
    ↓
Install Dependencies
    ↓
Run Tests
    ↓
Build Docker Image
    ↓
Docker Image

## 📂 Project Structure

jenkins-ci-cd-nodejs/
│
├── Jenkinsfile
├── Dockerfile
├── .dockerignore
├── .gitignore
├── package.json
├── package-lock.json
├── server.js
└── README.md

## ⚙️ Jenkins Pipeline

The Jenkins pipeline is defined inside the `Jenkinsfile`.

Jenkins connects to the GitHub repository and uses the Jenkinsfile to execute the pipeline automatically.

The pipeline contains the following stages:

### 1. Checkout

Jenkins downloads the latest source code from the GitHub `main` branch.

### 2. Install Dependencies

Jenkins installs all required Node.js packages using:

npm ci

### 3. Test

Jenkins runs the application tests using:

npm test

If the test fails, the pipeline stops.

### 4. Build Docker Image

After the tests are successful, Jenkins builds the Docker image using the Dockerfile.

Command used:

docker build -t ci-cd-nodejs-app:latest .

## 🐳 Docker

Docker is used to package the Node.js application into a container.

Build the image manually:

docker build -t ci-cd-nodejs-app:latest .

Run the container:

docker run -p 3000:3000 ci-cd-nodejs-app:latest

The application can then be accessed at:

http://localhost:3000

## 🌐 Application

The application is a simple Node.js Express server.

Home page:

http://localhost:3000

Response:

Hello! My CI/CD Pipeline is working 🚀

Health check:

http://localhost:3000/health

Response:

{"status":"OK"}

## 🔐 Jenkins Configuration

Jenkins was configured to connect with the GitHub repository.

The Jenkins Pipeline job uses:

Repository:
https://github.com/kirthika25160/jenkins-ci-cd-nodejs.git

Branch:

main

Pipeline file:

Jenkinsfile

Jenkins automatically executes the stages defined in the Jenkinsfile.

## 📦 Docker Hub

Docker Hub is used to store the Docker image.

Docker Hub repository:

https://hub.docker.com/r/kirthika2516/ci-cd-nodejs-app

Docker image:

kirthika2516/ci-cd-nodejs-app:latest

## ✅ Result

The Jenkins pipeline was successfully executed.

The pipeline automatically performs:

Code Checkout → Install Dependencies → Test → Docker Build

The Jenkins build completed successfully with a green build status.

## 🎓 What I Learned

Through this task, I learned:

- Jenkins and Jenkins pipelines
- Jenkinsfile
- GitHub integration with Jenkins
- CI/CD concepts
- Automated testing
- Docker image building
- Running Node.js applications using Docker
- Jenkins pipeline stages
- Basic Jenkins configuration

## 💡 Key DevOps Concept

Jenkins helps automate repetitive development and deployment tasks.

Instead of manually downloading the code, installing dependencies, running tests, and building the Docker image, Jenkins performs these steps automatically through the pipeline.

## 👩‍💻 Author

**Kirthika**

GitHub:
https://github.com/kirthika25160
