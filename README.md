
![image](https://github.com/user-attachments/assets/825cff3a-0ee2-47fa-afb5-b991dcbeee65)


# Salary API Documentation

| Author        | Date       | Version | Review Level   | Reviewer Name        | 
|---------------|------------|---------|----------------|----------------------|
| Anitha Annem  | May 03   | v1.0   | Pre-Reviewer   | Priyanshu            |
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
The **Salary API** is a vital microservice in the [OT-Microservices](OT-Microservices) project, handling employee salary data and transactions. It operates independently, integrating with other services like Employee and Attendance APIs. Designed for high performance, scalability, and reliability, it is optimized for cloud environments and follows modern development practices.

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
![image](https://github.com/user-attachments/assets/cdb6ce44-0db5-4468-acd0-c24c1b838f66)


# ScyllaDB

Refer this link for the deatiled documentation [ScyllaDB](https://github.com/Cloud-NInja-snaatak/Documentation/blob/aniruddh_SCRUM-111/ot_ms_understanding/software/database/scylladb/documentation/README.md)
 
  
# Redis

Refer this link for the deatiled documentation [Redis](https://github.com/Cloud-NInja-snaatak/Documentation/blob/SHREY-SCRUM-107/ot_ms_understanding/software/middleware/redis/documentation/README.md)
  
# Migrate
Refer this link for the deatiled documentation[Migrate](https://github.com/Cloud-NInja-snaatak/Documentation/blob/anitha_scrum42/commonstack/dependencies/migrate/documentation.md)


  
# Maven

Refer this link for the deatiled documentation [Maven](https://github.com/Cloud-NInja-snaatak/Documentation/blob/kanika_scrum26/commonstack/applications/java/maven/documentation.md)

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



