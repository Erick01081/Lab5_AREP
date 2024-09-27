# Property Management CRUD System

A web-based CRUD (Create, Read, Update, Delete) system for managing real estate properties. This project allows users to perform basic operations on property listings through a user-friendly interface.

## Table of Contents
1. [Project Summary](#project-summary)
2. [System Architecture](#system-architecture)
3. [Class Design](#class-design)
4. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installing](#installing)
5. [Deployment](#deployment)
6. [Running the Tests](#running-the-tests)
7. [Built With](#built-with)
8. [Authors](#authors)
9. [License](#license)
10. [Acknowledgments](#acknowledgments)

## Project Summary

This Property Management System is a web application that enables users to:
- Create new property listings
- View a list of all properties and individual property details
- Update existing property information
- Delete property listings

The system consists of a frontend built with HTML and JavaScript, a backend REST API developed using Spring Boot, and a MySQL database for data persistence.

## System Architecture

The system follows a three-tier architecture deployed on AWS:

1. **Frontend**: HTML + JavaScript
   - Runs in the client's browser
   - Communicates with the backend API using AJAX or Fetch API

2. **Backend**: Spring Boot REST API
   - Deployed on EC2 instance 1
   - Exposes RESTful endpoints for CRUD operations
   - Handles business logic and data validation
   - Interacts with the database using JPA/Hibernate

3. **Database**: MySQL
   - Hosted on EC2 instance 2
   - Stores property data in a `properties` table

## Class Design

Key classes in the system include:

1. `Property`: Represents a real estate property with attributes such as ID, address, price, size, and description.
2. `PropertyService`: Handles business logic for property management.
3. `PropertyController`: Exposes REST endpoints for property operations.
4. `PropertyRepository`: Interfaces with the database for data persistence.

## Getting Started

These instructions will help you set up the project on your local machine for development and testing purposes.

### Prerequisites

- Java Development Kit (JDK) 11 or later
- Node.js and npm
- MySQL Server
- Maven
- Git

### Installing

1. Clone the repository:
   ```
   git clone https://github.com/Erick01081/Lab5_AREP.git
   ```

2. Navigate to the project directory:
   ```
   cd Lab5_AREP
   ```

3. Set up the database:
   - Create a new MySQL database named `property_management`
   - Update `application.properties` in the `src/main/resources` directory with your database credentials

4. Build and run the backend:
   ```
   mvn spring-boot:run
   ```
5. Access the application at `http://localhost:8080`


## Deployment

To deploy the system on AWS:

1. Set up an EC2 instance (Instance 1) for the Spring Boot backend service
2. Set up another EC2 instance (Instance 2) for the MySQL database
3. Configure security groups to allow necessary traffic between the instances and from the internet to Instance 1
4. Deploy the frontend HTML/JS files to Instance 1 or serve them from a separate web server
5. Start the Spring Boot service on Instance 1
6. Ensure MySQL is running and properly configured on Instance 2

Detailed deployment instructions:

### Architecture Diagram

![image](https://github.com/user-attachments/assets/b27f4cd3-eb89-4136-86e5-e45062185833)

## Video

https://github.com/user-attachments/assets/49b35172-c615-429e-9136-4133afcf1b6e

### Extra credits

![image](https://github.com/user-attachments/assets/5dea885f-7820-4bb7-a301-865b4d5f699c)

## Running the Tests

Explain how to run the automated tests for this system:

```
mvn test
```

## Built With

* [Spring Boot](https://spring.io/projects/spring-boot) - The backend framework
* [React](https://reactjs.org/) - The frontend library
* [MySQL](https://www.mysql.com/) - Database
* [Maven](https://maven.apache.org/) - Dependency Management
* [npm](https://www.npmjs.com/) - Package Manager for JavaScript

## Authors

Erick Montero




