# Book My Ticket — Movie Ticket Booking System

A full-stack movie ticket booking web application built with Java and Spring Boot. The application has separate user and admin workflows for browsing movies, managing shows, selecting seats, and booking tickets.

## Technology Stack
- Java 17, Spring Boot, Spring MVC
- Spring Data JPA, Hibernate, MySQL
- Thymeleaf, HTML, CSS, Bootstrap
- Redis (configured for caching/session-related functionality)
- JavaMailSender for email/OTP workflows
- Razorpay for payment integration
- Cloudinary for movie/theater image storage
- ZXing for QR-code generation

## Features
- User registration, login, and email OTP verification
- Browse movies, theaters, and show timings
- Seat selection and booking workflow
- QR-code ticket generation
- Admin workflows for managing movies, theaters, screens, seats, shows, and users
- Payment integration with Razorpay (requires valid credentials and configuration)
- Image upload integration with Cloudinary (requires valid credentials)

> Features and integrations depend on the local configuration and credentials. Do not commit real credentials, API keys, passwords, or production data.

## Prerequisites
- JDK 17
- Maven 3.8+ (or use the Maven wrapper if present)
- MySQL
- Redis, if using the Redis-backed functionality

## Local Setup
1. Clone this repository.
2. Create a MySQL database named `book_my_ticket` (or update the datasource URL).
3. Copy `src/main/resources/application.properties.example` to `src/main/resources/application.properties`.
4. Add your own local database, mail, admin, Cloudinary, and Razorpay settings as required by the code. Keep this local properties file untracked.
5. Run the application with `./mvnw spring-boot:run` (Windows: `mvnw.cmd spring-boot:run`) or `mvn spring-boot:run`.
6. Open `http://localhost:8088` in your browser.

## Project Structure
- `src/main/java` — application code, controllers, services, repositories, entities, and utilities
- `src/main/resources/templates` — Thymeleaf HTML templates
- `src/main/resources/static` — static assets
- `src/test/java` — automated tests

## Security Notes
- Keep `application.properties` and `.env` files out of Git.
- Use environment variables or a secret manager for credentials.
- Configure secure admin credentials before running outside a local development environment.
- Payment integrations must verify payment signatures server-side.

## Author
Ankitha H.
