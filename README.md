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
| Containerization| Docker (multi-stage build) |

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

### Run locally

```bash
mvn spring-boot:run
```

Requires a PostgreSQL instance on `localhost:5432` with a `cashcard` database.

### Run with Docker Compose

```bash
docker compose up -d
```

Starts both the application and PostgreSQL. The API is available at `http://localhost:8080`.

To stop and remove everything:

```bash
docker compose down -v
```

### Environment Variables

| Variable      | Default                                      | Description         |
|---------------|----------------------------------------------|---------------------|
| `DB_URL`      | `jdbc:postgresql://localhost:5432/cashcard`   | JDBC connection URL |
| `DB_USERNAME` | `postgres`                                   | Database username   |
| `DB_PASSWORD` | `postgres`                                   | Database password   |

## License

This project is for educational purposes.
