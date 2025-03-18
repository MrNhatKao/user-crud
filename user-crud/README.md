# User CRUD API

A simple RESTful API for managing users built with Spring Boot.

## Technologies Used

- Java
- Spring Boot
- Spring Data JPA
- Hibernate
- Maven
- JUnit 5
- MockMvc

## Project Overview

This application provides a complete set of CRUD (Create, Read, Update, Delete) operations for managing user data. It includes validation for user input and appropriate error handling.

## Project Structure

```
user-crud/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/user_crud/
│   │   │       ├── controller/
│   │   │       ├── model/
│   │   │       ├── repository/
│   │   │       ├── common/
│   │   │       └── UserCrudApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/
│           └── com/example/user_crud/
│               └── UserControllerIntegrationTest.java
└── pom.xml
```

## API Endpoints

| Method | URL | Description |
|--------|-----|-------------|
| GET | /users | Get all users |
| GET | /users/{id} | Get user by ID |
| POST | /users | Create a new user |
| PUT | /users/{id} | Update an existing user |
| DELETE | /users/{id} | Delete a user |

## User Model

```json
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com",
  "age": 30
}
```

## Validation

- Name: Cannot be blank
- Email: Cannot be blank, must be a valid email format
- Age: Optional

## Setup Instructions

1. Clone the repository
2. Configure the database connection in `application.properties`
3. Run `mvn clean install` to build the project

## Running the Application

```bash
mvn spring-boot:run
```

The API will be available at `http://localhost:8080`

## Running Tests

```bash
mvn test
```

## License

[MIT](https://choosealicense.com/licenses/mit/)