# Jenkins Spring Boot Demo

A simple Java 17 + Spring Boot REST API used to learn Jenkins CI/CD.

## Endpoint

After starting the application, open:

- `http://localhost:8080/hello`

Expected response:

```text
Hello from Spring Boot! Jenkins CI is coming.
```

## Run locally

```bash
mvn clean package
mvn spring-boot:run
```

## Technologies

- Java 17
- Spring Boot
- Maven
- JUnit 5
