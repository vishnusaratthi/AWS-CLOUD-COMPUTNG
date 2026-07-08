Day 7 – Jenkins CI/CD Pipeline with Docker Deployment

Project Objective

The objective of this project is to implement an automated Continuous Integration and Continuous Deployment (CI/CD) pipeline for a Flask Hospital Application using Jenkins, Docker, GitHub, Docker Hub, and AWS EC2. The purpose of this project is to eliminate manual deployment activities and enable faster, reliable, and efficient application delivery.

Through this project, whenever changes are made in the source code repository, Jenkins automatically performs the required tasks such as fetching source code, building Docker images, pushing images to Docker Hub, and deploying the updated application.

Technologies Used

AWS EC2 (Ubuntu Server)
Used as a cloud-based virtual machine to host Jenkins and deploy the application.

Jenkins
Used as a CI/CD automation tool to build, test, and deploy applications automatically.

GitHub
Used as a source code management platform for storing application files and Jenkins pipeline configuration.

Docker
Used to containerize the Flask application and ensure consistent deployment across environments.

Docker Hub
Used as a centralized repository for storing Docker images.

Python Flask
Used as the backend web framework to create the Hospital application.

Project Architecture

The project follows the below workflow:

GitHub Repository
↓
Jenkins Pipeline Trigger
↓
Source Code Checkout
↓
Docker Image Build
↓
Docker Hub Login
↓
Push Image to Docker Hub
↓
Deploy Container on EC2
↓
Flask Hospital Application Running


Tasks Completed

1. Created AWS EC2 Instance

The first step involved creating an Ubuntu EC2 instance in AWS cloud.

Steps performed:

Logged into AWS Console.

Selected EC2 service.

Launched Ubuntu instance.

Configured security groups.

Opened required ports:


Port 22 → SSH access
Port 8080 → Jenkins
Port 5000 → Flask Application

Connected to the instance using SSH:

ssh -i key.pem ubuntu@public-ip

Purpose:

EC2 acts as the server where Jenkins and Docker are installed.


2. Jenkins Installation

Jenkins was installed on the Ubuntu EC2 instance.

Commands used:

sudo apt update

sudo apt install openjdk-17-jdk -y

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install jenkins -y

Started Jenkins service:

sudo systemctl start jenkins

sudo systemctl enable jenkins

Checked status:

sudo systemctl status jenkins

Accessed Jenkins:

http://<EC2-Public-IP>:8080

Purpose:

Jenkins automates software development and deployment processes.


3. Docker Installation

Docker was installed for container creation and deployment.

Commands used:

sudo apt install docker.io -y

sudo systemctl start docker

sudo systemctl enable docker

Added Jenkins user to Docker group:

sudo usermod -aG docker jenkins

Restarted Jenkins:

sudo systemctl restart jenkins

Purpose:

Docker helps package the application with all required dependencies.


4. Created GitHub Repository

A GitHub repository was created and application source code was uploaded.

Repository includes:

Flask application files

Dockerfile

Jenkinsfile

Requirements.txt

HTML templates


Purpose:

GitHub serves as the central repository for source code management.


5. Created Docker Hub Repository

Docker Hub repository created:

savitha0209/flask-hospital-app

Purpose:

Stores Docker images generated from Jenkins pipeline.

Benefits:

Central image storage

Easy deployment

Image version management

6. Configured Jenkins Pipeline

Created a Jenkins Pipeline project:

flask-hospitalapp

Configuration included:

GitHub repository URL

Branch selection

Jenkinsfile path

Docker Hub credentials


Purpose:

Allows Jenkins to execute automated stages.


7. Pipeline Execution Process

The Jenkins pipeline executed multiple stages:

Stage 1: Checkout Source Code

Jenkins connects to GitHub and downloads application files.

Stage 2: Build Docker Image

Docker image created:

docker build -t flask-hospital-app .

Stage 3: Login into Docker Hub

Authentication performed:

docker login

Stage 4: Push Docker Image

Image pushed:

docker push savitha0209/flask-hospital-app

Stage 5: Remove Existing Container

Old container removed:

docker rm -f hospital-container

Stage 6: Run New Container

New container created:

docker run -d -p 5000:5000 --name hospital-container savitha0209/flask-hospital-app

Purpose:

Ensures latest application version is always deployed.


Application Deployment

The Flask Hospital application was deployed successfully.

Application URL:

http://<EC2-Public-IP>:5000

Features of Hospital Application:

Patient registration

Doctor details

Appointment handling

User interface using Flask templates

Web-based access


Output

Successfully achieved the following:

✔ Jenkins pipeline executed successfully

✔ Source code fetched from GitHub

✔ Docker image built successfully

✔ Docker image pushed to Docker Hub

✔ Docker container created successfully

✔ Flask Hospital application deployed successfully

✔ Application accessible using EC2 public IP


---

Screenshots Included

AWS EC2 Running Instance

Jenkins Dashboard

Jenkins Console Output

Docker Hub Repository

Docker Installation Output

Flask Hospital Application Running

EC2 Terminal Configuration

Docker Container Running

Jenkins Pipeline Stages

Learning Outcomes

Through this project, the following concepts were learned:

AWS EC2 server setup

Jenkins installation and configuration

Docker installation and management

GitHub integration with Jenkins

Docker Hub repository usage

CI/CD pipeline creation

Automated deployment process

Docker image creation

Container deployment techniques

Continuous Integration concepts

Continuous Deployment concepts


Conclusion

Successfully implemented a complete end-to-end CI/CD pipeline using Jenkins, Docker, GitHub, Docker Hub, and AWS EC2. The project automated the entire deployment workflow, reducing manual work and improving deployment speed and consistency.

This project demonstrates real-world DevOps practices by integrating various tools and technologies into a single automated pipeline. The implementation also provides hands-on experience in continuous delivery, infrastructure management, and application deployment strategies.

This expanded version should fit more like a 5–6 page report/book format.
