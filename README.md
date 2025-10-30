# hello-jumpstart

A Spring Boot 3.5.5 microservices architecture project using Java 25.

## Project Structure

This is a multi-module Maven project with the following structure:

```
hello-jumpstart/
├── pom.xml (parent POM)
├── main-app/ (Main Spring Boot application)
│   └── Health Check REST Controller
└── service/ (MSA services directory)
    ├── member-service/
    ├── billing-service/
    └── notification-service/
```

## Technology Stack

- **Java**: 25
- **Spring Boot**: 3.5.5
- **Build Tool**: Maven
- **Architecture**: Microservices (MSA)

## Services

### Main Application (Port 8080)
- Main Spring Boot application
- Provides health-check REST endpoint at `/api/health-check`

### Member Service (Port 8081)
- Member management microservice
- Located in `service/member-service`

### Billing Service (Port 8082)
- Billing management microservice
- Located in `service/billing-service`

### Notification Service (Port 8083)
- Notification management microservice
- Located in `service/notification-service`

## Prerequisites

- Java 25 or higher
- Maven 3.6+

## Building the Project

Build all modules:
```bash
mvn clean install
```

Build a specific module:
```bash
mvn clean install -pl main-app
```

## Running the Applications

### Main Application
```bash
cd main-app
mvn spring-boot:run
```

### Member Service
```bash
cd service/member-service
mvn spring-boot:run
```

### Billing Service
```bash
cd service/billing-service
mvn spring-boot:run
```

### Notification Service
```bash
cd service/notification-service
mvn spring-boot:run
```

## API Endpoints

### Health Check
- **URL**: `http://localhost:8080/api/health-check`
- **Method**: GET
- **Response**:
  ```json
  {
    "status": "UP",
    "message": "Application is running"
  }
  ```

## Testing

Run all tests:
```bash
mvn test
```

Run tests for a specific module:
```bash
mvn test -pl main-app
```