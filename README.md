# Vprofile Application

A Java-based web application built with Spring Framework, deployed via a GitOps CI/CD pipeline.

## Tech Stack

- Java 21 / Spring MVC
- MySQL, Memcached, RabbitMQ
- Maven for build and dependency management
- Docker for containerization
- SonarQube for code quality analysis
- Amazon ECR for container registry
- Helm for Kubernetes deployment

## CI/CD Pipeline

### On Pull Request to `main`
- Build and unit tests via Maven
- Checkstyle report generation
- SonarQube code quality scan
- SonarQube quality gate check

### On Push to `main`
- Docker image build and push to Amazon ECR
- Helm values update in the GitOps repository

## Local Development

### Prerequisites
- Java 21
- Maven 3.x
- Docker

### Build
```bash
mvn clean package -DskipTests
```

### Run tests
```bash
mvn test
```
