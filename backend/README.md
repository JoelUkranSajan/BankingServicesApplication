# Backend - Financial Management System

This is the backend application for the Financial Management System(Banking System). It is responsible for handling all API requests and managing the microservices for accounts, cards, and loans similar to banking service. The backend is built using **Spring Boot** and deployed as Docker containers.

---

## Features
- Handles accounts, cards, and loans microservices.
- Integrated with Eureka for service discovery.
- Configured with a central configuration server.
- Uses health checks for reliable service operation.

---

## Prerequisites
To set up and run the backend, ensure you have the following installed:
- **Java** (JDK 11 or higher)
- **Docker** and **Docker Compose**
- **Curl** (optional, for testing endpoints)

---

## Microservices Overview
The backend consists of the following microservices:

1. **Config Server**: Provides centralized configuration for other services.
2. **Eureka Server**: Manages service discovery.
3. **Accounts Service**: Handles account-related operations.
4. **Cards Service**: Handles card-related operations.
5. **Loans Service**: Handles loan-related operations.
6. **Gateway Server**: Acts as a gateway for routing requests to the respective services.

---

## Local Development Setup

Follow these steps to set up the backend application for local development:

### 1. Clone the Repository
```bash
git clone <https://gitlab.com/philip29cyriac/financial-management-system-db.git>
cd backend
```
### 2. Create the Network
Before running the application, create the required Docker network:

```bash
docker network create eazybank
```
### 3. Build and Start the Application
To build the application and start the container, run the following command:
```bash
docker-compose up --build
```

## Microservice Endpoints
Here are the default ports for each microservice:

1. **Config Server**: [http://localhost:8071](http://localhost:8071)  
2. **Eureka Server**: [http://localhost:8070](http://localhost:8070)  
3. **Accounts Service**: [http://localhost:8081](http://localhost:8081)  
4. **Cards Service**: [http://localhost:8090](http://localhost:8090)  
5. **Loans Service**: [http://localhost:9000](http://localhost:9000)  
6. **Gateway Server**: [http://localhost:8072](http://localhost:8072)

## Health Check
Each microservice has a health check endpoint for monitoring:

```bash
http://<service-host>:<port>/actuator/health
```
**Example**
To check the health of the Accounts Service:

```bash
curl http://localhost:8081/actuator/health