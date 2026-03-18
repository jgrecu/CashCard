# CashCard

A RESTful API service for managing family cash cards -- digital debit cards designed for families to manage allowances. Built with Spring Boot, Spring Security, and Spring Data JDBC.

## Features

- **CRUD Operations** -- Create, read, update, and delete cash cards via REST endpoints
- **Authentication & Authorization** -- HTTP Basic authentication with role-based access control (Spring Security)
- **Owner Isolation** -- Users can only access their own cash cards
- **Pagination & Sorting** -- Configurable pagination with default sorting by amount
- **Data Persistence** -- Spring Data JDBC with PostgreSQL
- **Database Migrations** -- Flyway for versioned schema management
- **Integration Testing** -- Testcontainers with real PostgreSQL instances

## Tech Stack

| Component       | Technology              |
|-----------------|-------------------------|
| Framework       | Spring Boot 4.0.3       |
| Language        | Java 25                 |
| Security        | Spring Security         |
| Data Access     | Spring Data JDBC        |
| Database        | PostgreSQL              |
| Migrations      | Flyway                  |
| Testing         | Testcontainers (PostgreSQL) |
| Build Tool      | Maven                   |

## API Endpoints

| Method | Endpoint                  | Description             |
|--------|---------------------------|-------------------------|
| GET    | `/api/v1/cashcards/{id}`  | Retrieve a cash card    |
| GET    | `/api/v1/cashcards`       | List all cash cards     |
| POST   | `/api/v1/cashcards`       | Create a new cash card  |
| PUT    | `/api/v1/cashcards/{id}`  | Update a cash card      |
| DELETE | `/api/v1/cashcards/{id}`  | Delete a cash card      |

## Getting Started

### Prerequisites

- Java 25+
- Maven 3.9+
- Docker or Podman (for tests)
- PostgreSQL (for production)

### Build & Test

```bash
mvn clean package
```

### Run

```bash
mvn spring-boot:run
```

## License

This project is for educational purposes.
