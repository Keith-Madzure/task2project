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
