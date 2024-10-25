# Project Overview: Microservices Architecture

## Features Completed

### 1. **Microservices Architecture**
- **Service-Oriented Architecture**: 
  - The backend is divided into multiple microservices:
    - **auth-service**: Handles user authentication and validation (Node.js).
    - **train-service**: Manages train information (Django).
    - **ticket-service**: Facilitates the ticket booking process (Node.js).
    - **pricing-service**: Manages ticket pricing (Node.js).
    - **cache-service**: Manages ticket availability and ticket booking process locking at the cache level (Node.js).
    - **web-service**: Serves the UI (Node.js).
  - Each service is developed in separate repositories and operates independently.

### 2. **Inter-Service Communication**
- **HTTP Requests**: 
  - Microservices communicate via HTTP requests, invoking operations or accessing shared data as needed.
- **Middleware Integration**: 
  - Middleware is implemented for handling HTTP requests, event publishing, and consumption to maintain a clean separation of concerns and promote reusability.

---

### 3. **Containerization and Deployment Configurations**
- **Containerization with Docker**: 
  - The client (frontend) and backend microservices are containerized using Docker to ensure consistent deployment across different environments.
  
- **Cloud Deployment with Kubernetes**: 
  - All services are deployed on DigitalOcean’s Kubernetes cluster.
  - Kubernetes Deployment and Service YAML files are utilized for managing application lifecycle and networking.

- **Horizontal Pod Autoscaling (HPA)**: 
  - HPA is configured for all microservices to automatically scale based on CPU utilization, ensuring optimal performance under varying loads.

- **Resource Limitation**: 
  - Resource limits are applied to all deployments to prevent resource exhaustion.

---

### 4. **Testing**
- **Functional Testing**: 
  - Comprehensive test suites are written for the microservices using Jest and Supertest, ensuring functionality and integration testing for APIs.
  
- **Load Testing**: 
  - Managed with k6, creating test loads on services.

- **Performance Testing**: 
  - Managed with k6, simulating performance under load.

---

### 5. **Monitoring**
- **Metrics Monitoring**: 
  - Prometheus and Grafana are integrated to monitor the health and performance of the system locally, providing insights into resource utilization and metrics.
  
- **HPA Monitoring**: 
  - HPA configurations and status can be monitored effectively.

---

### 6. **Database**
- **PostgreSQL Cluster**: 
  - PostgreSQL is utilized as the database, hosted on DigitalOcean.

- **Redis Caching**: 
  - Redis is deployed with Kubernetes and used for caching in the backend services.

---

### 7. **Cloud Deployment**
- **Domain Registration and Configuration**: 
  - Registered and configured the domain **district12.xyz** through NameCheap for seamless access to the application.

- **Deployment with Ingress and Kong**: 
  - Deployed the full website using an Ingress controller with Kong and Helm, effectively managing routing for multiple subdomains.

- **Preflight Request Handling and CORS Configuration**: 
  - Implemented CORS policies to properly handle preflight requests, ensuring secure communication between the client and backend services.

- **HTTPS Protocol**: 
  - Configured Ingress, Cluster Issuer, and Cert-Manager to switch from HTTP to HTTPS protocol.

---

### 8. **Continuous Integration and Deployment**
- **GitHub Actions**: 
  - Continuous integration and deployment pipelines are set up using GitHub Actions, although further testing is required.

---

### 9. **Monitoring Tools**
- **Prometheus Integration**: 
  - Prometheus is deployed alongside the cloud infrastructure to monitor the performance and health of the microservices.

- **Grafana Integration**: 
  - Grafana is deployed alongside the cloud infrastructure to visualize the performance and health of the microservices.

---

## Conclusion
This project showcases a robust microservices architecture with advanced deployment and monitoring configurations, ensuring high availability, scalability, and maintainability.