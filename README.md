# 🛍️ ShopVerse – Event-Driven E-Commerce Platform

---

## 🚀 Overview

**ShopVerse** is a production-level, event-driven e-commerce backend built with **Java 17** and **Spring Boot**.  
It demonstrates how to design **scalable microservices** with real-world tools and integrations — exactly like modern product-based companies do.

---

## 🧱 Architecture

            ┌──────────────────────────────┐
            │        API Gateway           │
            │ (JWT Auth + Rate Limiting)   │
            └─────────────┬────────────────┘
                          │
 ┌────────────────────────┴────────────────────────┐
 │               │               │                 │
User Service Product Service Order Service Payment Service
│ │ │ │
PostgreSQL MongoDB+Elastic PostgreSQL Kafka Events
│ │ │ │
└──────────────► Redis ◄────────┴─────────────────┘
▲
│
Notification Service (Kafka Consumer)


---

## ⚙️ Tech Stack

| Category | Tools / Frameworks |
|-----------|--------------------|
| Language | Java 17 |
| Framework | Spring Boot 3, Spring Data JPA, Spring Security |
| Messaging | Apache Kafka |
| Databases | PostgreSQL, MongoDB |
| Search | ElasticSearch |
| Caching | Redis |
| Containerization | Docker, Docker Compose |
| Cloud | AWS EC2 (Free Tier) |
| CI/CD | GitHub Actions |
| Monitoring | Prometheus + Grafana |
| Fault Tolerance | Resilience4J |

---

## 🧩 Microservices Overview

| Service | Description |
|----------|--------------|
| **User Service** | Handles user management and authentication (PostgreSQL + JWT) |
| **Product Service** | Product catalog and search (MongoDB + ElasticSearch) |
| **Order Service** | Creates and manages orders (Kafka + PostgreSQL) |
| **Payment Service** | Processes payments asynchronously |
| **Notification Service** | Sends alerts based on Kafka events |
| **API Gateway** | Central entry point with rate limiting and security |

---

## 🧠 Key Features

- ✅ Event-Driven Architecture using **Kafka**
- 🔒 JWT Authentication & Authorization
- ⚡ Redis caching + rate limiting
- 🧩 ElasticSearch-powered product search
- 🛡️ Circuit breaker (Resilience4J)
- 🐳 Dockerized microservices
- ☁️ AWS EC2 deployment (Free Tier)
- 🔁 CI/CD pipeline using GitHub Actions

---

## 💻 Setup & Run (Free Tools Only)

### 1️⃣ Clone the repository
```bash
git clone https://github.com/aditisingh98/shopverse-microservices.git
cd shopverse-microservices
