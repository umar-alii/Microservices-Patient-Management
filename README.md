# Microservices-Patient-Management
Microservices Based Patient Management System.



This is a comprehensive **Spring Boot Microservices** project simulating a **Healthcare Management System**, where microservices like **Patient Service**, **Billing Service**, **Analytics Service**, **Auth Service**, and an **API Gateway** are integrated using modern practices like **gRPC**, **Kafka**, **Docker**, **OpenAPI**, and **AWS** infrastructure provisioning via **CloudFormation**.

---

## 📖 Project Overview

This application is designed to demonstrate how to build and scale a real-world enterprise microservices system using:

- Spring Boot for service creation
- gRPC for synchronous service communication
- Kafka for asynchronous communication and event-driven architecture
- Docker for containerization
- API Gateway for centralized routing and authentication
- JWT for authentication and authorization
- AWS CloudFormation for Infrastructure as Code (IaC)
- Integration testing using Spring's testing framework

---

## 🧰 Tools & Technologies Used

| Category                  | Tool / Tech                          |
|---------------------------|--------------------------------------|
| Language & Framework      | Java 17, Spring Boot 3               |
| API Protocols             | REST, gRPC                           |
| Messaging Queue           | Apache Kafka                         |
| Security & Auth           | Spring Security, JWT                 |
| Database                  | PostgreSQL, H2 (Memory DB)           |
| Testing                   | JUnit, Mockito, Spring Boot Test     |
| Containerization          | Docker                               |
| Documentation             | OpenAPI (Swagger)                    |
| Cloud & Infrastructure    | AWS, LocalStack, AWS CLI             |
| IaC                       | AWS CloudFormation                   |
| API Gateway               | Spring Cloud Gateway                 |
| Build Tools               | Maven                                |
| gRPC Codegen              | Protocol Buffers (protobuf)          |

---

## 📁 Microservices Breakdown

### 🧍 Patient Service
- REST endpoints to manage patient records
- Validations, exception handling
- Produces Kafka events for analytics
- Consumes gRPC Billing Service

### 💳 Billing Service
- gRPC server to handle billing requests
- Interacts with Patient Service via gRPC

### 📊 Analytics Service
- Kafka consumer
- Processes patient events for analytics
- Stores analytics records (or logs for now)

### 🔐 Auth Service
- Manages login and JWT generation
- Integration with API Gateway for route protection

### 🌐 API Gateway
- Central entrypoint for all external requests
- Routes traffic to underlying services
- Validates JWTs via Auth Service

---

## 🧪 Testing
- Unit tests for services and controllers
- Integration tests for Auth and Patient modules

---

## 🚢 Deployment
- Docker Compose for local containerization
- LocalStack to emulate AWS locally
- CloudFormation for provisioning:
  - VPC
  - ECS Cluster
  - MSK (Kafka)
  - Load Balanced API Gateway

---

