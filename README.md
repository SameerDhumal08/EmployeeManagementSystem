# Employee Management System with CI/CD Pipeline

A Full Stack Employee Management System developed using React, Spring Boot, MySQL, Docker, GitHub Actions, Docker Hub, and AWS EC2.

# Project Overview

This project demonstrates a complete DevOps workflow by automating the build, packaging, deployment, and hosting of a full-stack application.

The application allows users to:

Add Employees
View Employee Records
Store Employee Data in MySQL Database
Access the application through a web browser

The project is containerized using Docker and deployed automatically to AWS EC2 using GitHub Actions CI/CD pipelines.

---
# Architecture
```
Developer
    |
    | Git Push
    v
GitHub Repository
    |
    v
GitHub Actions
    |
    +-- Build Frontend Docker Image
    +-- Build Backend Docker Image
    +-- Push Images to Docker Hub
    |
    v
AWS EC2 Instance
    |
    +-- Frontend Container
    +-- Backend Container
    +-- MySQL Container
    |
    v
Docker Compose
```
# Technologies Used

## Frontend
- React.js
- Axios
- Bootstrap
- JavaScript
- JSX

## Backend
- Spring Boot
- Spring Data JPA
- Hibernate
- REST API
- Maven

## Database
- MySQL

## DevOps

Docker
Docker Compose
GitHub Actions
Docker Hub
AWS EC2
Elastic IP

---

# Features

Employee Management
Add Employee
Fetch Employee Details
Store Data in MySQL Database

##DevOps Features

Automated CI/CD Pipeline
Dockerized Frontend
Dockerized Backend
Dockerized MySQL Database
Automated Docker Image Push to Docker Hub
Automated Deployment to AWS EC2
Persistent MySQL Storage using Docker Volumes

##CI/CD Workflow

Continuous Integration

When code is pushed to the main branch:

1. GitHub Actions starts automatically
2. Builds Backend Docker Image
3. Builds Frontend Docker Image
4. Pushes Images to Docker Hub
5. Continuous Deployment

After successful image creation:

1. GitHub Actions connects to AWS EC2 via SSH
2. Pulls latest Docker images
3. Stops old containers
4. Deploys updated containers using Docker Compose

---
# 📸 Application Screenshots

## Employee List Page

<p align="center">
  <img width="1913" height="901" alt="allemployees" src="https://github.com/user-attachments/assets/6f1f0b95-1a02-492b-b536-df8e87bab185" />

</p>

---

## Add Employee Page

<p align="center">
  <img width="1918" height="911" alt="addems" src="https://github.com/user-attachments/assets/a6936102-9fcd-4d90-ad62-620da27c09e3" />

</p>

---

## Update Employee Page

<p align="center">
  <img width="1919" height="910" alt="updateems" src="https://github.com/user-attachments/assets/3add2aa1-2ffa-4b2a-9f1d-73114db3b564" />

</p>

---
## Department List Page

<p align="center">
<img width="1911" height="925" alt="Screenshot 2026-05-30 091317" src="https://github.com/user-attachments/assets/c02f8df4-2a9a-46a3-847d-25b23a521a7a" />

</p>

---
## Add Department Page

<p align="center">
  <img width="1919" height="914" alt="Screenshot 2026-05-30 091333" src="https://github.com/user-attachments/assets/15ab0601-2e0c-4f7b-8756-09b2fed16905" />
 />

</p>

---

## Update Department Page

<p align="center">
<img width="1919" height="917" alt="Screenshot 2026-05-30 091403" src="https://github.com/user-attachments/assets/be97eb88-c099-4c7f-b28b-26a47581408f" />

</p>

---
## Docker Images
<img width="1667" height="107" alt="docker images" src="https://github.com/user-attachments/assets/84059742-870d-4e49-8275-1c74a778c196" />

---

##Docker Compose Services

  MySQL
  Image: mysql:8.0
  Port: 3306

  Backend
  Spring Boot Application
  Port: 8080
  
  Frontend
  React Application
  Port: 80
  <img width="517" height="655" alt="image" src="https://github.com/user-attachments/assets/3051fbae-7739-41ac-b4a5-65f38ef220b7" />

---
##Database Persistence

MySQL data persistence is achieved using Docker Volumes.

volumes:
  mysql-data:

This ensures that employee records remain available even after:

Container restart
EC2 reboot
Application redeployment

---
##AWS Deployment

Infrastructure:

  AWS EC2 Ubuntu Instance
  <img width="1918" height="865" alt="image" src="https://github.com/user-attachments/assets/b131bb62-34a6-4545-8594-de6edd4852f4" />

  
  Elastic IP
  <img width="1917" height="727" alt="elastic ip association" src="https://github.com/user-attachments/assets/0cea8aab-4469-4dcb-ac2d-56101e43b025" />

  Docker Engine
  
  Docker Compose
  <img width="722" height="896" alt="dockerfile on ec2 to run workflow" src="https://github.com/user-attachments/assets/670b5a21-0823-4526-bbf8-c037ef84be3e" />

---

##GitHub Secrets Used

  DOCKERHUB_USERNAME
  DOCKERHUB_TOKEN
  EC2_HOST
  EC2_USERNAME
  EC2_SSH_KEY

---

##GitHub Actions Workflow

The CI/CD pipeline performs:

Source Code Checkout
Docker Hub Authentication
Docker Image Build
Docker Image Push
AWS EC2 Deployment
<img width="1857" height="835" alt="image" src="https://github.com/user-attachments/assets/4917684a-a746-4c44-85e7-f1144dbddbb4" />

---

##Learning Outcomes

Through this project, I gained hands-on experience with:

Docker Containerization
Docker Compose
GitHub Actions
CI/CD Pipeline Implementation
Docker Hub Registry
AWS EC2 Deployment
Spring Boot Deployment
React Deployment
MySQL Persistence
DevOps Best Practices

---
# 📸 Application Architecture

```text
+----------------------+
|   User Browser       |
+----------+-----------+
           |
           | Access Application
           |
+----------v-----------+
|    React Frontend    |
|      Port: 3000      |
|  React + Axios + UI  |
+----------+-----------+
           |
           | Axios HTTP Requests
           |
+----------v-----------+
|   Spring Boot API    |
|      Port: 8080      |
| REST Controllers/API |
+----------+-----------+
           |
           | JPA / Hibernate
           |
+----------v-----------+
|      MySQL DB        |
|      Port: 3306      |
+----------------------+

```
---

##Author

Sameer Dhumal

GitHub: https://github.com/SameerDhumal08
LinkedIn: www.linkedin.com/in/sameerdhumal14

