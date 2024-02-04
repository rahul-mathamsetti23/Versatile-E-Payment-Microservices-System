# E-Payment System

A comprehensive e-wallet system that enables users to effortlessly transfer amounts, view their balance, recent transactions, and manage account settings. Developed with a microservices architecture and integrated with modern technologies ensuring responsive and secure user interactions.

<img width="803" alt="image" src="https://github.com/anudeep2804/E_Wallet_Microservice_Application/assets/68229062/f2049546-4f6c-47d8-850b-e706ea7509b6">

## Features

- **P2P Transfers**: Allow users to send money to other registered users.
- **Account Management**: Fetch balance, view recent transactions, and edit account settings.
- **Email Notifications**: Automated emails upon every transaction event.
- **Admin Functionalities**: Endpoints for admins to fetch user details.

## Microservices

1. **User Service**: Handle user creation, updates, and queries.
2. **Transaction Service**: Oversee transaction initiation and processing.
3. **Notification Service**: Administer transactional email notifications.
4. **Wallet Service**: Manage user wallet balances and updates.

> Note: All services are interconnected efficiently using Kafka.

## Technologies

- **Spring Boot**: Backend microservices framework.
- **Kafka**: Real-time data streaming for inter-service communication.
- **OAuth**: Authentication and authorization.
- **Spring Security**: Secure the endpoints.
- **JPA**: Data management and persistence.
- **Databases**: Independent databases for each microservice.

## Controller Insights

### Transaction Controller (`TxnController`)

- 🔗 **Endpoint**: `/txn`
  - **Method**: POST
  - **Description**: Initiate a P2P transaction.
  - **Parameters**: `receiver`, `purpose`, `amount`.

### User Controller (`UserController`)

- 🔗 **Endpoint**: `/user`
  - **Method**: POST
  - **Description**: Register a new user.
- 🔗 **Endpoint**: `/user`

  - **Method**: GET
  - **Description**: Fetch authenticated user details.

- 🔗 **Endpoint**: `/admin/all/users`

  - **Method**: GET
  - **Description**: Get details of all registered users (admin only).

- 🔗 **Endpoint**: `/admin/user/{userId}`
  - **Method**: GET
  - **Description**: Retrieve specific user details using their ID (admin only).

## Setup & Installation

1. **Clone**: Download the repository.
2. **Databases**: Configure individual databases for each service.
3. **Environment**: Update `application.properties` with relevant credentials.
4. **Kafka**: Ensure the Kafka server is operational.
5. **Run**: Build and initiate each microservice using Spring Boot.
