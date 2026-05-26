
# First REST API — Spring Boot Project (Task 2)

A REST API built with Spring Boot for the Akademia Finansów i Biznesu Vistula course. The project demonstrates how to design a clean, layered REST API with full CRUD support, exception handling, API documentation, and database integration using Spring Data JPA.

## What this project covers

- Creating a Spring Boot project directly from IntelliJ using Spring Initializr
- Building a layered architecture (Controller → Service → Repository) with proper package separation
- Implementing full **CRUD** operations on a `Product` resource (Create, Read, Update, Delete)
- Mapping between request/response DTOs and domain objects using a dedicated mapper
- Centralized exception handling with `@ControllerAdvice` and custom exceptions
- API documentation and testing via **Swagger UI** (OpenAPI)
- Persisting data using **Spring Data JPA**, **Hibernate**, and an in-memory **H2 database**

## Tech stack

- **Java** (latest stable version)
- **Spring Boot** with the following dependencies:
  - Spring Web
  - Spring Data JPA
  - H2 Database
  - Spring Boot DevTools
  - SpringDoc OpenAPI (Swagger UI)
- **Maven** as the build tool

## Project structure

```
src/main/java/.../firstrestapispring/
 ├── product/
 │    ├── api/                  # ProductController
 │    │    ├── request/         # ProductRequest, UpdateProductRequest
 │    │    └── response/        # ProductResponse
 │    ├── domain/               # Product entity
 │    ├── service/              # ProductService (business logic)
 │    ├── repository/           # ProductRepository (JpaRepository)
 │    └── support/              # ProductMapper, ProductExceptionAdvisor,
 │         └── exception/       #   ProductExceptionSupplier, ProductNotFoundException
 ├── shared/api/response/       # ErrorMessageResponse (shared DTO)
 └── FirstRestApiSpringApplication.java
```

## How to run

1. Clone the repository:
   ```bash
   git clone https://github.com/Keith-Madzure/YOUR_REPO_NAME.git
   ```
2. Open the project in IntelliJ IDEA.
3. Let Maven reload and download all dependencies.
4. Run the main class `FirstRestApiSpringApplication`.
5. The app will start on `http://localhost:8080`.


## Useful URLs

- **Swagger UI:** http://localhost:8080/swagger-ui/index.html
- **OpenAPI JSON:** http://localhost:8080/v3/api-docs
- **H2 Database Console:** http://localhost:8080/console
  - JDBC URL: `jdbc:h2:mem:testdb`

## Testing the API

You can test the endpoints using:
- **Swagger UI** (built-in, easiest)
- **Postman** or **Insomnia**
- A regular browser (for GET requests only)

Example `POST` body:
```json
{
  "name": "Sample product"
}
