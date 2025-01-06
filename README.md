# Financial Management System - Overview

This repository contains the **Financial Management System**, a full-stack application designed to manage user accounts, cards, and loans. The project is divided into two main components:

- **Backend**: Built using a microservices architecture to handle the core business logic and data storage.
- **Frontend**: A Next.js-based user interface for seamless interaction with the backend services.

---

## System Overview

The **Backend** is composed of multiple microservices:

- **Config Server**: Manages configurations for all services.
- **Eureka Server**: Acts as the service discovery server.
- **Accounts Service**: Handles user accounts.
- **Cards Service**: Manages credit/debit card data.
- **Loans Service**: Handles loan-related operations.
- **Gateway Server**: Serves as the entry point to route requests to appropriate microservices.

The **Frontend** provides the user-facing interface for interacting with the backend services. It allows users to register, log in, view, and manage accounts, cards, and loans.

---

## Prerequisites

To set up the Financial Management System, ensure you have the following installed:

- **Node.js** (v18 or higher)
- **Docker** and **Docker Compose**

---

## Running the Application

### Step 1: Start the Backend

The backend services must be running before starting the frontend. Follow the steps in the backend's [README file](./backend/README.md) for detailed instructions on how to set up and run the backend microservices.

1. Clone the repository.
2. Navigate to the backend folder.
3. Use Docker Compose to build and run the services.

### Step 2: Start the Frontend

Once the backend is up and running, set up the frontend by following the instructions in the frontend's [README file](./frontend/README.md). Ensure the frontend is connected to the same Docker network as the backend.

---

## Key Notes

- The backend services must be fully operational for the frontend to function correctly. If the backend is not running, the frontend will fail to fetch data or process user requests.
- Each component (frontend and backend) has its own dedicated README file with specific setup instructions, file structure details, and available endpoints.

---

## Individual Component Documentation

- [Frontend README](./frontend/README.md): Instructions for setting up and running the frontend application.
- [Backend README](./backend/README.md): Instructions for setting up and running the backend microservices.

---

By following the steps outlined in the respective README files, you can easily set up and run the Financial Management System. Ensure to start the backend first to avoid any connectivity issues with the frontend.