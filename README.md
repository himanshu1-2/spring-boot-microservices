# E-Commerce Microservices Project

## Overview

This project is a Spring Boot-based microservices architecture for an e-commerce platform. It includes services for inventory, orders, and products. Key features include service discovery with Eureka, authentication with Keycloak, messaging with Kafka, API gateway implementation, circuit breaker pattern, and distributed tracing using Zipkin. Testing is facilitated using Testcontainers.

## Microservices

### 1. Inventory Service
Manages product stock levels.

### 2. Order Service
Handles order processing and management.

### 3. Product Service
Manages product information.

## Key Technologies

- **Spring Boot**: Core framework for building microservices.
- **Eureka**: Service discovery.
- **Keycloak**: Authentication and authorization.
- **Kafka**: Messaging and notification service.
- **Spring Cloud Gateway**: API Gateway implementation.
- **Resilience4j**: Circuit breaker implementation.
- **Zipkin**: Distributed tracing.
- **Testcontainers**: Integration testing.

## Architecture Diagram

![Architecture Diagram](path/to/diagram.png)

## Project Setup

### Prerequisites

- Java 11
- Docker
- Maven
- Keycloak
- Kafka
- Eureka Server
- Zipkin Server

### Running the Services

 # Start Eureka Server**
   cd eureka-server
   mvn spring-boot:run

# Start Keycloak
docker run -d -p 8080:8080 --name keycloak jboss/keycloak

# Start Kafka
docker-compose -f kafka-docker-compose.yml up

# Start Zipkin
docker run -d -p 9411:9411 openzipkin/zipkin

# Start Inventory Service
cd inventory-service
mvn spring-boot:run

# Start Order Service
cd order-service
mvn spring-boot:run

# Start Product Service
cd product-service
mvn spring-boot:run

# Start API Gateway
cd api-gateway
mvn spring-boot:run
