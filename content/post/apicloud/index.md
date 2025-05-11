---
title: Creating an API with Express and deploying to the cloud with AWS
description: Academic project | Developing a REST API with Express, JWT authentication, SQLite and deploying to AWS with Packer and Terraform
slug: api-express-aws
date: 2025-03-10 00:00:00+0000
image: apicloud.png
categories:
- Backend Development
- Cloud Computing
tags:
- Node.js
- Express
- REST API
- JWT
- SQLite
- AWS
- EC3
- RDS
- Packer
- Terraform

weight: 1
---

This project was developed as part of the subject Server-Side Technologies: Cloud Computing within the Master's Degree in Mobile Computing (MIMO). The objective was to implement a complete REST API using **Node.js and Express**, with authentication using **JWT**, persistence in **SQLite**, and deployment on **AWS** following good scalability and automation practices.

## Project objectives

- Implement a REST API according to an **OpenAPI** specification.
- Manage authentication and authorization with **JWT**.
- Implement **CRUD** operations for movie and rating resources.
- Apply data validations and proper handling of HTTP status codes.
- Deploy the API on **AWS** with a scalable and automated infrastructure using **Packer** and **Terraform**.

## Main functionalities

### 1. Authentication and security

- **Login endpoint** (`POST /sessions`) to generate JWT tokens.
- Protect sensitive routes using **authentication middleware**.
- Handling authentication errors with appropriate responses (`401 Unauthorized`).

### 2. Movie management (`/movies`)

- **GET /movies**: Returns all movies with required fields (ID, title, genre, duration, rating).
- **Optional pagination** to improve efficiency in large queries.
- **Error handling** with appropriate responses (`404 Not Found`, `500 Internal Server Error`).

### 3. Rating management (`/ratings`)

- **Full CRUD** so users can create, read, update, and delete ratings.
- **Validations**:
- `rating` must be between **0 and 5**.
- `comments` with a maximum of **500 characters**.
- **Access restrictions**:
- Only authenticated users can modify or delete their ratings.
- Error handling with appropriate codes (`401 Unauthorized`, `422 Unprocessable Entity`, `201 Created`).

### 4. Watchlist management (`/watchlist`)

- Allows users to add and manage movies to watch.
- Validation of **Movie IDs** before adding them.
- Handling of watched/unwatched movie statuses.
- **Appropriate responses**:
- `409 Conflict` for duplicate movies.
- `422 Unprocessable Entity` for invalid IDs.
- `404 Not Found` for non-existent movies.

## Technical implementation

### **Technologies used**
- **Node.js + Express**: Development of the REST API.
- **SQLite**: Lightweight and efficient database.
- **JWT (jsonwebtoken)**: Authentication implementation.
- **Docker**: Containerization of the development environment.
- **AWS (EC2, S3, IAM)**: Cloud infrastructure.
- **Packer**: Creation of AMI images for AWS.
- **Terraform**: Automation of cloud deployment.

### **Persistence and database**
- Use of **SQLite** to store user, movie, and rating information.
- **Migrations and defined schema** to ensure data integrity.
- **ORM Sequelize** to facilitate database management.

### **Deployment on AWS**

#### **1. Creating AMI with Packer**
An **Amazon Machine Image (AMI)** was generated with the necessary configuration to run the API:
- Installation of **Node.js** and dependencies.
- Configuration of the environment and necessary variables.
- Creation of a script for automatic execution of the service.

#### **2. Infrastructure with Terraform**
The infrastructure was implemented with **Terraform**, ensuring scalability and automation:
- **EC2 instance** configured with the generated AMI.
- **Load balancer** to distribute traffic.
- **Auto Scaling Group** to increase or decrease instances on demand.
- **RDS storage** for data persistence in the cloud.
- **IAM role and permission management** to ensure security.

### **Automation and scalability**
- **Autoscaling infrastructure** that allows adjusting the number of instances based on load.
- **Error handling** to ensure high availability and minimize downtime.
- **Data persistence** ensured with storage in AWS.

## Conclusions and learnings
This project allowed us to consolidate knowledge in **backend development with Express**, JWT authentication, **SQL** databases, as well as in **cloud infrastructure and deployment automation** in AWS. Good security practices, data validations and error handling were applied, achieving a robust and scalable system.

## Resources and source code
- [GitHub repository](https://github.com/israelbrea12/Despliegue-API-express-AWS.git)
- [OpenAPI documentation](/mimo_movies.yaml)