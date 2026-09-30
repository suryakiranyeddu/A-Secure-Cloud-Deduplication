# A-Secure-Deduplication-of-Textual-Data

A Java/JSP-based secure cloud textual data management system demonstrating **data encryption, access control, key management, transaction monitoring, and data deduplication concepts**.

## Overview

The system provides different roles for managing and accessing protected cloud data:

* **Data Owner** - manages and stores data.
* **End User** - requests access and downloads authorized data.
* **Key Authority (KGC)** - manages secret-key related operations.
* **Cloud Server** - handles cloud-side storage and access validation.
* **Attacker/Revocation** - handles unauthorized or blocked users.

## Main Features

* User registration and authentication
* Secure data access workflow
* AES-based data encryption
* Secret-key request and management
* Access validation
* Attacker/revocation handling
* Transaction logging
* Data deduplication concepts

## System Workflow

```text
Data Owner
    |
    v
Cloud Storage
    |
    v
End User
    |
    | Request Secret Key
    v
Key Authority (KGC)
    |
    | Authorization
    v
Cloud Server
    |
    +---- Authorized ----> Decrypt / Download
    |
    +---- Unauthorized --> Attacker / Revocation
```

## Technologies Used

* Java
* JSP
* JDBC
* MySQL
* HTML / CSS / JavaScript
* AES Encryption
* RSA Key-Pair Generation
* Apache Tomcat

## Screenshots

### End User Registration

![End User Registration](Screenshots/end-user-registration.png)

### Key Authority Dashboard

![Key Authority Dashboard](Screenshots/key-authority-dashboard.png)

### End User Dashboard

![End User Dashboard](Screenshots/end-user-dashboard.png)

## Project Structure

```text
A-Secure-cloud-deduplication/
│
├── JSP Pages
├── Database Connectivity
├── Security Components
├── Screenshots/
├── README.md
└── .gitignore
```

## Database

The application uses **MySQL** with the project database:

```text
aesd
```

JDBC is used for communication between the JSP application and MySQL.

## Local Setup

Required:

* Java JDK
* Apache Tomcat 9
* MySQL
* MySQL JDBC Driver

Basic setup:

```text
Java/JSP Application
        |
       JDBC
        |
      MySQL
```

Configure the local database connection before running the application.

## Security Concepts

The project demonstrates:

* Secure cloud storage concepts
* Encryption-based data protection
* Secret-key management
* User authentication
* Access authorization
* Transaction monitoring
* Attacker/revocation handling
* Data deduplication concepts

## Application Modules

### End User Module

* User registration
* Authentication
* Secret key request
* Data access request
* Authorized download

### Key Authority Module

* Secret key management
* User monitoring
* Attacker record management

### Cloud Server Module

* Data storage
* Access validation
* Secure data retrieval

## Running the Project

1. Install Java JDK.
2. Install Apache Tomcat 9.
3. Install MySQL.
4. Create the required database.
5. Configure JDBC connection.
6. Deploy the project in Tomcat.
7. Start the Tomcat server.
8. Open the application in a browser.

Example:

```text
http://localhost:8080/SecureCloud/
```

## Project Benefits

* Demonstrates secure cloud data handling.
* Shows encryption and authorization workflow.
* Provides role-based access management.
* Demonstrates key management concepts.
* Includes monitoring of transactions and unauthorized users.

## Note

This is a **legacy JSP-based project for demonstration and learning purposes**.

Production deployment would require additional improvements such as secure password hashing, proper secret management, stronger key management, input validation, secure session handling, and modern application architecture.
