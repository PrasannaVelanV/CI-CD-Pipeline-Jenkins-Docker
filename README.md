# CI/CD Pipeline for Java Web Application using Jenkins & Docker

Automated Build • Continuous Integration • Continuous Deployment • Java • Maven • Jenkins • Docker • Tomcat 9

---

# 📖 Project Overview

This project demonstrates the implementation of a complete **CI/CD (Continuous Integration and Continuous Deployment) Pipeline** for a Java-based **Online Bookstore** web application using **Jenkins**, **Maven**, **Docker**, and **Apache Tomcat 9**.

The pipeline automates the entire software delivery lifecycle—from source code integration to application deployment. Whenever a developer pushes code to GitHub, Jenkins automatically builds the project, packages it into a WAR file using Maven, creates a Docker image, and deploys the application inside a Tomcat 9 Docker container.

This project showcases real-world DevOps practices by reducing manual deployment effort, improving consistency, and enabling faster software delivery.

---

# 🏗️ Architecture Diagram

> **Insert the CI/CD Architecture Diagram here**

```
Developer
     │
     │ Git Commit & Push
     ▼
GitHub Repository
     │
     │ Webhook Trigger
     ▼
Jenkins CI Server
     │
     │ mvn clean package
     ▼
Maven Build
     │
     │ Generates WAR
     ▼
Docker Build
     │
     │ Creates Docker Image
     ▼
Docker Image
     │
     │ docker run
     ▼
Tomcat 9 Docker Container
     │
     ▼
Online Bookstore Web Application
```

---

# 🚀 Workflow

### 1. Code Development

The developer writes or updates the Java source code for the Online Bookstore application and pushes the changes to the GitHub repository.

### 2. GitHub Webhook

GitHub automatically triggers Jenkins through a webhook whenever new code is pushed.

### 3. Jenkins Pipeline

Jenkins starts the CI/CD pipeline by pulling the latest source code and executing the configured build stages.

### 4. Maven Build

Jenkins runs the following command:

```bash
mvn clean package
```

This command compiles the project, downloads dependencies, executes the build lifecycle, and generates the **OnlineBookstore.war** artifact.

### 5. Docker Image Creation

Jenkins builds a Docker image using the generated WAR file.

```bash
docker build -t online-bookstore .
```

The Docker image contains:

* Apache Tomcat 9
* OnlineBookstore.war
* Java Runtime Environment

### 6. Application Deployment

Jenkins deploys the application by starting a Docker container.

```bash
docker run -d -p 8080:8080 online-bookstore
```

### 7. Application Access

After deployment, the application is available at:

```
http://localhost:8080/OnlineBookstore
```

---

# 🛠️ Technologies Used

| Technology      | Purpose                                        |
| --------------- | ---------------------------------------------- |
| Java            | Application Development                        |
| Maven           | Build Automation & Dependency Management       |
| Git             | Version Control                                |
| GitHub          | Source Code Repository                         |
| Jenkins         | Continuous Integration & Continuous Deployment |
| Docker          | Containerization                               |
| Apache Tomcat 9 | Java Web Application Server                    |
| Linux           | Deployment Environment                         |

---

# ✨ Features

* Automated CI/CD pipeline using Jenkins
* GitHub webhook integration
* Automated Maven build process
* WAR artifact generation
* Docker image creation
* Containerized deployment using Tomcat 9
* One-click automated deployment
* Faster software delivery
* Reduced manual deployment errors
* Consistent deployment environment

---

# 📂 Project Structure

```text
CI-CD-Pipeline-Jenkins-Docker/
│
├── Screenshots/
│
├── OnlineBookstore/
│   ├── src/
│   ├── pom.xml
│   ├── Dockerfile
│   ├── Jenkinsfile
│   └── target/
│
├── CI-CD-Pipeline-Jenkins-Docker.pdf
├── README.md
└── LICENSE
```

---

# ⚙️ Prerequisites

Before running this project, ensure the following software is installed:

* Java JDK 8 or later
* Apache Maven
* Git
* GitHub Account
* Jenkins
* Docker Desktop / Docker Engine
* Apache Tomcat 9 (inside Docker)

Verify installations:

```bash
java -version
mvn -version
git --version
docker --version
jenkins --version
```

---

# 🚀 Deployment Steps

## Clone the Repository

```bash
git clone https://github.com/PrasannaVelanV/CI-CD-Pipeline-Jenkins-Docker-OnlineBookstore.git
```

```bash
cd CI-CD-Pipeline-Jenkins-Docker-OnlineBookstore
```

---

## Configure Jenkins

* Create a new Jenkins Pipeline project.
* Connect the GitHub repository.
* Configure the GitHub webhook.
* Add the Maven installation.
* Configure Docker on the Jenkins server.

---

## Build the Project

Jenkins automatically executes:

```bash
mvn clean package
```

---

## Build Docker Image

```bash
docker build -t online-bookstore .
```

---

## Deploy Docker Container

```bash
docker run -d -p 8080:8080 online-bookstore
```

---

## Access the Application

Open your browser and visit:

```
http://localhost:8080/OnlineBookstore
```

---

# 📸 Project Screenshots

Include screenshots such as:

* GitHub Repository
* Jenkins Dashboard
* Jenkins Build Console Output
* Successful Maven Build
* Docker Images
* Running Docker Container
* Tomcat Deployment
* Online Bookstore Home Page

---

# 🔄 CI/CD Pipeline Summary

```
Developer
      │
      ▼
GitHub Repository
      │
Webhook Trigger
      ▼
Jenkins Pipeline
      │
      ▼
Maven Build
      │
      ▼
WAR Artifact
      │
      ▼
Docker Build
      │
      ▼
Docker Image
      │
      ▼
Docker Container
      │
      ▼
Tomcat 9
      │
      ▼
Live Online Bookstore Application
```

---

# 🎯 Skills Demonstrated

* Continuous Integration (CI)
* Continuous Deployment (CD)
* Jenkins Automation
* Maven Build Automation
* Docker Containerization
* Git & GitHub
* Java Web Application Deployment
* Apache Tomcat Administration
* Linux System Administration
* DevOps Workflow Implementation

---

# 🔮 Future Enhancements

* Add SonarQube for code quality analysis
* Integrate JUnit automated testing
* Push Docker images to Docker Hub
* Deploy using Kubernetes
* Configure Nginx Reverse Proxy
* Add Prometheus and Grafana monitoring
* Deploy on AWS EC2
* Implement Blue-Green Deployment
* Add Email Notifications in Jenkins

---

# 🧹 Clean Up

Stop and remove the running container:

```bash
docker stop <container_id>
docker rm <container_id>
```

Remove the Docker image:

```bash
docker rmi online-bookstore
```

---

# 👨‍💻 Author

**Prasanna Velan**

**GitHub:**
https://github.com/PrasannaVelanV

**LinkedIn:**
https://www.linkedin.com/in/prasannavelanv

**Portfolio:**
https://github.com/PrasannaVelanV

---

# ⭐ Support

If you found this project useful, consider giving this repository a **⭐ Star** on GitHub. Your support helps showcase the project and motivates future improvements.

Thank you for visiting! 🚀
