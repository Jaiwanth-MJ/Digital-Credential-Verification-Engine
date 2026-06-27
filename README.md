# 🔐 Digital Credential Verification Engine

A secure and scalable **Spring Boot REST API** for managing, verifying, and auditing digital credentials. The application provides JWT-based authentication, role-based authorization, credential verification workflows, audit logging, and RESTful APIs documented with Swagger.

---

## 📌 Features

- User Registration & Login
- JWT Authentication
- Role-Based Authorization (ADMIN, VERIFIER, VIEWER)
- Credential Holder Management
- Credential Record Management
- Verification Rule Management
- Credential Verification Workflow
- Audit Trail Logging
- RESTful APIs
- Swagger/OpenAPI Documentation
- Exception Handling
- Layered Architecture
- Hibernate/JPA Integration
- MySQL Database
- TestNG & Mockito Unit Testing

---

# 🏗️ Project Architecture

```
Client
   │
   ▼
REST Controllers
   │
   ▼
Service Layer
   │
   ▼
Repository Layer
   │
   ▼
MySQL Database
```

Authentication Flow

```
User
 │
 ▼
Login
 │
 ▼
Authentication Manager
 │
 ▼
JWT Token Generated
 │
 ▼
Protected APIs
```

---

# 📂 Project Structure

```
src
 ├── main
 │   ├── java
 │   │   └── com.example.demo
 │   │        ├── config
 │   │        ├── controller
 │   │        ├── dto
 │   │        ├── entity
 │   │        ├── exception
 │   │        ├── repository
 │   │        ├── security
 │   │        ├── service
 │   │        ├── servlet
 │   │        └── DemoApplication.java
 │   │
 │   └── resources
 │        └── application.properties
 │
 └── test
```

---

# 🚀 Technologies Used

| Technology | Purpose |
|------------|----------|
| Java 17 | Programming Language |
| Spring Boot | Backend Framework |
| Spring Security | Authentication & Authorization |
| JWT | Secure Authentication |
| Hibernate | ORM Framework |
| Spring Data JPA | Database Operations |
| MySQL | Database |
| Maven | Dependency Management |
| Swagger/OpenAPI | API Documentation |
| TestNG | Unit Testing |
| Mockito | Mock Testing |
| Servlet API | Status Endpoint |

---

# 🔒 Authentication

The application uses **JWT (JSON Web Token)** authentication.

### Roles

- ADMIN
- VERIFIER
- VIEWER

Protected APIs require a valid JWT token in the Authorization header.

```
Authorization: Bearer <JWT_TOKEN>
```

---

# 📖 API Modules

## Authentication

- Register User
- Login User

---

## Credential Holder

- Create Holder
- Get Holder
- Update Holder Status
- List Holders

---

## Credential Record

- Create Credential
- Update Credential
- Get Credential
- Search by Holder
- Search by Credential Code

---

## Verification Rules

- Create Rule
- View Rules

---

## Verification Request

- Initiate Verification
- Process Verification
- View Verification Requests

---

## Audit Trail

- Log Verification Events
- View Credential Logs

---

# 🗄️ Database

The application uses **MySQL** as the relational database.

Major entities include:

- User
- Credential Holder Profile
- Credential Record
- Verification Rule
- Verification Request
- Audit Trail Record

Relationships are implemented using Hibernate/JPA annotations.

---

# 📄 Swagger API Documentation

After starting the application, Swagger UI is available at:

```
http://localhost:9001/swagger-ui/index.html
```

OpenAPI JSON

```
http://localhost:9001/v3/api-docs
```

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/Jaiwanth-MJ/Digital-Credential-Verification-Engine.git
```

---

## Navigate to Project

```bash
cd Digital-Credential-Verification-Engine
```

---

## Configure Database

Create a MySQL database.

Update:

```
application.properties
```

with your:

- Database URL
- Username
- Password
- JWT Secret

---

## Build Project

```bash
mvn clean install
```

---

## Run Application

```bash
mvn spring-boot:run
```

or

```bash
mvn clean spring-boot:run
```

---
---

# 🔐 Security Features

- JWT Authentication
- Stateless Session Management
- Password Encryption
- Role-Based Authorization
- Protected REST APIs
- Secure Endpoint Configuration
---
# 📈 Future Enhancements

- Exception Handling Implementation
- Role Handling Implementation

# 👨‍💻 Author

**Jaiwanth MJ**

GitHub:
https://github.com/Jaiwanth-MJ

---

# 📜 License

This project is intended for educational and portfolio purposes.
