# Employee Management System

A Full Stack Employee Management System built using modern web technologies and containerized with Docker. The project also includes a CI/CD pipeline using GitHub Actions for automated build and deployment workflows.

A Full Stack Employee Management System developed using:

- React.js
- Spring Boot
- MySQL
- Docker
- Docker Compose

---

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

## DevOps / Containerization
- Docker
- Docker Compose

---

# Features

## Employee Operations
- Add Employee
- Get All Employees
- Update Employee
- Delete Employee

## Frontend Features
- Employee Table UI
- API Integration using Axios
- React Hooks (`useState`, `useEffect`)
- Responsive Bootstrap Design

## Backend Features
- REST APIs
- Layered Architecture
- DTO & Mapper Pattern
- JPA Repository

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

## CI/CD Pipeline (GitHub Actions)

This project uses GitHub Actions to automate the build and containerization process.

Pipeline Workflow
Developer pushes code to the main branch.
GitHub Actions workflow is triggered automatically.
Backend and Frontend Docker images are built.
Images are tagged and pushed to Docker Hub.
Updated images are ready for deployment using Docker Compose.

## CI/CD Tools Used

GitHub Actions
Docker
Docker Hub

## Docker Containers Running

<p align="center">
  <img src="" width="900"/>
</p>

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

🐳 Docker & CI/CD Architecture
```text
+---------------------------------------------------------------+
|                     GitHub Repository                         |
+-----------------------------+---------------------------------+
                              |
                              | Push to main
                              v
+---------------------------------------------------------------+
|                  GitHub Actions CI/CD Pipeline                |
|      Checkout → Build → Docker Build → Docker Push            |
+-----------------------------+---------------------------------+
                              |
                              | Push Docker Images
                              v
+---------------------------------------------------------------+
|                        Docker Hub                             |
+-----------------------------+---------------------------------+
                              |
                              | Pull Images
                              v
+---------------------------------------------------------------+
|                      Docker Compose                           |
+---------------------------------------------------------------+
          |                      |                       |
+---------v---------+  +---------v---------+  +----------v---------+
|   ems-frontend    |  |   ems-backend     |  |     mysql-db       |
|     React.js      |  |    Spring Boot    |  |       MySQL        |
|    Port: 3000     |  |    Port: 8080     |  |    Port: 3306      |
+-------------------+  +-------------------+  +--------------------+
```
---

# 📌 Future Enhancements
```text
JWT Authentication & Authorization
Role-Based Access Control (RBAC)
Swagger / OpenAPI Documentation
Kubernetes Deployment
AWS Cloud Deployment
Monitoring & Logging (Prometheus + Grafana)
```
---

# 👨‍💻 Author

Sameer Dhumal

GitHub:
https://github.com/SameerDhumal08
