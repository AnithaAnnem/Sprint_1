
![image](https://github.com/user-attachments/assets/825cff3a-0ee2-47fa-afb5-b991dcbeee65)


# Salary API Documentation

| Author        | Date       | Version | Review Level   | Reviewer Name        | 
|---------------|------------|---------|----------------|----------------------|
| Anitha Annem  | April 27   | v1.0   | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  |    |     | L0             | Khushi Malhothra      |
| Anitha Annem  |            |         | L1             | Rishabh Sharma       |
| Anitha Annem  |            |         | L2             | piyush Upadhyay      |

# Table of Contents
- [Salary API Overview](#salary-api-overview)
- [Purpose of the Salary API](#purpose-of-the-salary-api)
- [Architecture](#architecture)
- [ScyllaDB](#scylladb)
- [Redis](#redis)
- [Migrate](#migrate)
- [Maven](#maven)
- [Swagger](#swagger)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)
  
# Salary API Overview
The **Salary API** is a vital microservice in the **OT-Microservices** project, handling employee salary data and transactions. It operates independently, integrating with other services like Employee and Attendance APIs. Designed for high performance, scalability, and reliability, it is optimized for cloud environments and follows modern development practices.

# Purpose of the Salary API
The primary purpose of the Salary API is to streamline salary management processes within the organization.
| Aspect              | Description                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| Manage Salary Records | Manage and process salary records for employees.                                         |
| Integration         | Integrate easily with other microservices within the OT-Microservices ecosystem.          |
| Data Management     | Support efficient data storage, retrieval, and calculation related to employee compensation. |
| Automation and Accuracy | Automate payroll processes, enhancing accuracy in employee compensation records.     |
| Financial Operations | Simplify financial operations within the organization.                                    |

# Supported Features of the Salary API
- Built with **Spring Boot** and **Tomcat**
- Uses **ScyllaDB** for salary data storage
- Uses **Redis** for caching
- Uses **Prometheus/OpenTelemetry** for monitoring
- API documentation via **Swagger**
- Database migrations handled using **Migrate**

# Architecture
![Screenshot from 2025-05-03 20-06-04](https://github.com/user-attachments/assets/e30aef13-1660-47ea-b063-0bf0e8ac9362)


# ScyllaDB

**ScyllaDB** is a high-performance NoSQL database designed as a drop-in replacement for Apache Cassandra. It offers low-latency, high-throughput storage, optimized for scalable applications, and efficiently utilizes modern multi-core CPUs.

### Why ScyllaDB
- High performance with low latency
- Cassandra compatibility
- Automatic data sharding
- Automated database management (reduced manual tuning)
### Use Cases
- Real-time data collection in IoT applications (millions of devices)
- Large transaction processing with low latency in financial services (fraud detection, analytics)

  
# Redis
**Redis** is an open-source, in-memory data store used for caching, session management, and messaging. It supports various data structures and provides fast read/write performance.
### Why Redis
- Caching and session management
- Real-time messaging (Pub/Sub)
- Data persistence with fast retrieval
- Reduces database load and supports recovery after restarts
### Use Cases
- Web caching to improve response times
- Leaderboards for gaming/social media platforms
- Real-time analytics and event data aggregation (monitoring, ad tech)
  
# Migrate
**Migrate** is a database migration tool used to manage schema changes in evolving applications, especially in Go environments, ensuring consistent, version-controlled schemas across environments.
### Why Migrate
- Schema versioning and consistency
- Reversible migrations for safe deployment/rollback
- Automates migrations in CI/CD pipelines
### Use Cases
- Evolve schemas without manual SQL scripts
- Automate migrations in pipelines
- Manage schemas in multi-tenant applications
  
# Maven
**Maven** is a build automation and dependency management tool for Java applications, using a declarative `pom.xml` configuration.
### Why Maven
- Automates dependency management and build processes
- Standardizes project structures
- Supports plugins for testing, packaging, deployment
### Use Cases
- Automate Java project builds and dependency resolution
- Manage multi-module projects
- Integrate with CI tools like Jenkins for automated builds/tests

# Swagger
**Swagger** is an open-source toolset for designing, building, documenting, and testing RESTful APIs using the OpenAPI Specification (OAS).
## Key Benefits
- **Swagger UI** provides interactive API documentation
- Uses **OpenAPI Specification** for standardization
- Generates client SDKs in multiple languages
- Enhances collaboration between frontend and backend teams
### Core Components
- **Swagger UI** — Interactive documentation
- **Swagger Editor** — OpenAPI spec creation
- **Swagger Codegen** — Client SDKs and server stub generation
- **OpenAPI Specification (OAS)** — Standardized REST API documentation
### Common Use Cases
- Interactive API documentation and endpoint testing
- Client SDK generation
- Collaboration across teams via unified API specifications

# Conclusion
The **Salary API** in the OT-Microservices system efficiently manages salary transactions using:
- **ScyllaDB** for scalable storage
- **Redis** for caching
- **Migrate** for version control
- **Swagger** for documentation
- **Maven** for builds
It offers high performance, seamless integration with other microservices, and supports scalability and continuous deployment.

# Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|

# References

| **Link** | **Description** |
|----------|-----------------|
| [scylladb](https://www.scylladb.com/) | The documentation for this section is followed from this link. |
| [Redis](https://redis.io/) | The documentation for this section is followed from this link. |
| [migrate](https://github.com/golang-migrate/migrate) | The documentation for this section is followed from this link. |





