# Features Completed

## Microservices Architecture

### 1. Service-Oriented Architecture

- The backend is divided into multiple microservices:
  auth-service: handles user authenticaion and validatoin
  train-service: handles train information
  ticket-service: handles ticket booking process
  pricing-service: handles ticket pricing
  cache-service: handles ticket-availability and ticket-booking-process-locking at cache level, a wrapper service
  web-service: ui service

- Services are developed in separate repositories and works independently

### 2. Inter-Service Communication

#### HTTP Requests

- Microservices communicate via HTTP requests when necessary to invoke operations on another service or access shared data.

#### Middleware Integration

- Middleware is implemented for handling HTTP requests, event publishing, and event consumption to ensure clean separation of concerns and reusability.

## Containerization and Deployment Configurations

### 1. Containerization with Docker

- Client(front end) and backend microservices are containerized using Docker for consistent deployment across environments.

### 2. Cloud Deployment with Kubernetes

- All services are deployed on DigitalOcean’s Kubernetes cluster.
- Kubernetes Deployment and Service YAML files are used to manage application lifecycle and networking.

### 3. Horizontal Pod Autoscaling (HPA)

- HPA is configured for all microservices to automatically scale based on CPU utilization, ensuring optimal performance under varying loads.

### 4. Resource Limitation

- Resource limitation applied for all deployments to prevent exhaustion of resources.

## Testing

### 1. Functional Testing

- Comprehensive test suites are written for the microservices using Jest and Supertest, ensuring functionality and integration testing for APIs.

### 2. Load Testing

- Manged with k6 with test load created on services

### 3. Performance Testing

- Manged with k6 with test load created on services

## Monitoring

### 1. Metrics Monitoring

- Prometheus and Grafana are integrated to monitor the health and performance of the system locally, for a node server, providing insights into resource utilization and metrics

### 1. HPA Monitoring

- HPA Configuration and status can be monitored.

## Database

### 1. PostgreSQL cluster

- PostgreSQL is used for database with pg cluster hosted on DigitalOcean.

### 2. Redis Caching

- Redis is deployed with k8s and used for caching in the backend services.

## Cloud Deployment

### 1. Domain Registration and Configuration

- Registered and configured the domain district12.xyz through NameCheap for seamless access to the application.

### 2. Deployment with Ingress and Kong

- Deployed full website using an Ingress controller with Kong and Helm, managing routing for multiple subdomains effectively.

### 3. Preflight Request Handling and CORS Configuration

- Implemented CORS policies to properly handle preflight requests, ensuring secure communication between the client and backend services.

### 4. HTTPS Protocol

- Configured ingress, cluster issuer and cert-manager to switch to https protocol from http

## GitHub Actions

- Continuous integration and deployment pipelines are set up using GitHub Actions but require further testing.

## Prometheus Integration

- Prometheus is deployed alongside the cloud infrastructure to monitor the performance and health of the microservices.

## Grafana Integration

- Grafana is deployed alongside the cloud infrastructure to visualize the performance and health of the microservices.