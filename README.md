# Simple Library Management System - RESTful API

## Objective
The goal of this project is to enhance the Simple Library Management System by exposing it as a RESTful API using Spring Boot. This will help you understand how to design, develop, and implement a fully functioning REST API while applying key Spring Boot concepts.

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
    Description: Marks a book as borrowed.
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
