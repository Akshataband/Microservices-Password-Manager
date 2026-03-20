# 🔐 Rev Password Manager - Microservices Architecture

## 📌 Project Overview

Rev Password Manager is a **secure, scalable, cloud-native password management system** designed using **microservices architecture**.

The application allows users to safely store, manage, and analyze their credentials with **enterprise-level security features** like encryption, authentication, and security audits.

This project is a modernization of a **monolithic application** into a **distributed microservices system**, improving scalability, maintainability, and performance.

---

## 🚀 Key Features

* 🔐 Secure user authentication with JWT
* 🔒 AES encryption for password storage
* 🔑 Strong password generation with custom rules
* 📊 Password strength analysis & audit reports
* ⭐ Favorites, search, filter, and category management
* 🔔 Real-time notifications and security alerts
* 📥 Export/Import encrypted backups
* 🔐 Two-Factor Authentication (2FA)

---

## 🧩 Microservices Architecture

The system is divided into the following independent services:

### 1. User Service

* Authentication & Authorization
* JWT token generation
* Profile management
* 2FA and security questions

### 2. Vault Service

* Encrypted credential storage
* CRUD operations
* Search, filter, and favorites

### 3. Generator Service

* Strong password generation
* Custom rules (length, symbols, exclusions)

### 4. Security Service

* Password strength analysis
* Weak/reused password detection
* Audit reports
* Backup & restore

### 5. Notification Service

* Security alerts
* OTP & verification messages
* Event-based notifications

---

## 🏗️ System Architecture

Client (Angular UI)
↓
API Gateway
↓
-

## User | Vault | Generator | Security | Notification

```
    ↓  
```

Individual Databases

---

## 🔄 Application Flow

1. User sends request from UI
2. API Gateway routes request to appropriate service
3. User Service handles authentication and generates JWT
4. Vault Service stores encrypted passwords
5. Security Service analyzes password strength
6. Notification Service sends alerts if needed

---

## ☁️ Spring Cloud Components

### 🔹 Eureka Server (Service Discovery)

* Registers all microservices
* Enables communication using service names instead of URLs

### 🔹 API Gateway

* Single entry point
* Handles routing, authentication, and rate limiting

### 🔹 Config Server

* Centralized configuration management
* Avoids hardcoding properties

---

## 🔗 Inter-Service Communication

* Implemented using **OpenFeign Clients**
* Enables clean and easy REST communication between services

---

## 🔐 Security Implementation

* JWT-based authentication
* AES encryption for sensitive data
* 2FA (Two-Factor Authentication)
* Secure API access with filters

---

## 🧱 Tech Stack

### Backend

* Java 17
* Spring Boot 3
* Spring Cloud (Eureka, Gateway, Config)
* Spring Security
* Hibernate / JPA

### Frontend

* Angular
* TypeScript
* HTML, CSS

### Database

* MySQL

### DevOps & Tools

* Docker
* Maven
* Git

---

## 📁 Project Structure (Each Service)

* controller → Handles API requests
* service → Business logic
* repository → Database operations
* entity → Database models
* dto → Data transfer objects
* exception → Global exception handling
* config → Configuration classes

---

## 🏷️ Key Annotations Used

* `@SpringBootApplication` → Main class
* `@RestController` → REST APIs
* `@Service` → Business logic layer
* `@Repository` → Database layer
* `@Entity` → Database mapping
* `@Autowired` → Dependency injection
* `@FeignClient` → Service communication
* `@EnableEurekaClient` → Register service
* `@ControllerAdvice` → Global exception handling
* `@Valid` → Request validation

---

## 🐳 Docker Support

* Each microservice is containerized using Docker
* Enables easy deployment and environment consistency

---

## 🎯 Why Microservices?

* Independent deployment
* Better scalability
* Fault isolation
* Easier maintenance

---

## 📌 Future Enhancements

* Cloud deployment (AWS)
* Email/SMS integration
* Real-time breach detection
* Kubernetes orchestration

---

## 👩‍💻 Author

**Akshata Hemraj Band**
Full Stack Java Developer

---
