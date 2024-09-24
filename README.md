# Simple Library Management System - RESTful API

## Overview
This is a Spring Boot application for managing a library system, featuring functionalities to borrow and return books, as well as sending email notifications to users upon successful transactions.

## Features

- Manage books in the library (add, update, delete).
- Borrow and return books with notifications via email.
- Use PostgreSQL as the database.
- Asynchronous email sending using Spring Mail.

## Technologies Used

- **Java 17**
- **Spring Boot 2.x**
- **Spring Data JPA**
- **PostgreSQL**
- **Thymeleaf (optional for UI)**
- **JUnit 5 for testing**

  
## Project Setup

### Prerequisites
- Java 11 or higher
- Maven
- PostgreSQL

### Steps to Set Up the Project

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-directory>

### Run the Application
        mvn spring-boot:run
### Running Tests
        mvn test

### Logging
    SLF4J is used for logging throughout the application. You can configure logging levels in the application.properties file:

### properties

    logging.level.root=info
    logging.level.com._b.Service=debug
    logging.level.org.springframework=warn

### Monitoring with Spring Boot Actuator
-You can access the Actuator endpoints for monitoring:

   Health Check: http://localhost:8080/actuator/health
   Info: http://localhost:8080/actuator/info
### Unit Testing
   Unit tests are implemented using JUnit and Mockito. Mocking is used for dependencies in the service layer.

Conclusion
### API Endpoints
### Fetch All Books
     URL: /api/books
     Method: GET
     Description: Returns a list of all books.
### Fetch a Book by ID
     URL: /api/books/{id}
     Method: GET
     Description: Returns details of a specific book by ID.
### Add a New Book
     URL: /api/books
     Method: POST
     Description: Adds a new book to the library.
   
### Borrow a Book
    URL: /api/books/{id}/borrow
    Method: PUT
    Description: Marks a book as borrowed and mail will be send to admin.
### Return a Book
    URL: /api/books/{id}/return
    Method: PUT
    Description: Marks a book as returned.
### Delete a Book
    URL: /api/books/{id}
    Method: DELETE
    Description: Deletes a book from the library.
    
### Data Model
### Book Entity
    Fields:
         id (Long)
        title (String)
         author (String)
        isbn (String)
        isBorrowed (Boolean)

### Exception Handling
     404 Not Found: Book not found.
     400 Bad Request: Invalid input or operation (e.g., trying to borrow a book that’s already borrowed).
### Testing the API
    Use tools like Postman, curl, or Swagger UI to test each endpoint.
    Ensure that the API behaves as expected.
### Documentation
    The API documentation is generated using OpenAPI 3.0 and can be accessed via Swagger UI at /swagger-ui.html.
