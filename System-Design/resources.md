# System Design Resources

A curated collection of resources for learning System Design, Distributed Systems, Software Architecture, Scalability, Reliability, and Large-Scale System Design.

The resources are organized into YouTube videos, documentation, books, practice platforms, and important topics to study.

---

## YouTube Resources

| Resource                 | Topic                                                 | Link                                                   |
| ------------------------ | ----------------------------------------------------- | ------------------------------------------------------ |
| System Design Resource 1 | System Design Fundamentals                            | [Watch Video](https://youtu.be/SqcXvc3ZmRU)            |
| System Design Resource 2 | System Design                                         | [Watch Video](https://youtu.be/lFeYU31TnQ8)            |
| System Design Resource 3 | System Design                                         | [Watch Video](https://youtu.be/rN6cq8yyCas)            |
| System Design Resource 4 | System Design                                         | [Watch Video](https://youtu.be/lFeYU31TnQ8)            |
| System Design Resource 5 | System Design                                         | [Watch Video](https://youtu.be/fqySz1Me2pI)            |
| sudoCODE                 | System Design & Distributed Systems                   | [YouTube Channel](https://www.youtube.com/@sudocode)   |
| ByteByteGo               | System Design & Software Architecture                 | [YouTube Channel](https://www.youtube.com/@ByteByteGo) |
| Hussein Nasser           | Backend Engineering, Networking & Distributed Systems | [YouTube Channel](https://www.youtube.com/@hnasr)      |

---

## Important System Design Documentation

| Resource                                | Description                                                                          | Link                                                                                                                                                                               |
| --------------------------------------- | ------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Google SRE                              | Reliability, scalability, monitoring, distributed systems and production engineering | [Google SRE](https://sre.google/)                                                                                                                                                  |
| Google NALSD                            | Non-Abstract Large System Design methodology                                         | [Google NALSD](https://sre.google/workbook/non-abstract-design/)                                                                                                                   |
| Google SRE Book                         | Large-scale production systems and reliability engineering                           | [Read Online](https://sre.google/sre-book/table-of-contents/)                                                                                                                      |
| Google SRE Workbook                     | Practical SRE and system design practices                                            | [Read Online](https://sre.google/workbook/table-of-contents/)                                                                                                                      |
| AWS Well-Architected Framework          | Architecture, reliability, security, performance and cost optimization               | [AWS Documentation](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)                                                                                     |
| Google Cloud Architecture Center        | Cloud architecture patterns and best practices                                       | [Google Cloud Architecture](https://cloud.google.com/architecture)                                                                                                                 |
| Google Cloud Well-Architected Framework | Reliable, secure, efficient and scalable cloud architecture                          | [Documentation](https://docs.cloud.google.com/architecture/framework)                                                                                                              |
| AWS Distributed Systems Reliability     | Designing distributed systems to handle failures                                     | [AWS Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/design-interactions-in-a-distributed-system-to-mitigate-or-withstand-failures.html) |

---

## Distributed Systems Resources

| Topic                    | Resource                                                                                                                                                   |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Distributed Systems      | [Google SRE Distributed Systems Resources](https://sre.google/resources/)                                                                                  |
| Distributed Architecture | [Google Cloud Distributed Architecture Patterns](https://docs.cloud.google.com/architecture/hybrid-multicloud-patterns-and-practices/distributed-patterns) |
| Reliability              | [Google SRE](https://sre.google/sre-book/)                                                                                                                 |
| Scalability              | [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)                                                |

---

## Books

| Book                                                  | Author                        | Recommended For                                      |
| ----------------------------------------------------- | ----------------------------- | ---------------------------------------------------- |
| Designing Data-Intensive Applications                 | Martin Kleppmann              | Distributed Systems, Databases and Data Architecture |
| System Design Interview – An Insider's Guide          | Alex Xu                       | System Design Interview Fundamentals                 |
| System Design Interview – An Insider's Guide Volume 2 | Alex Xu                       | Advanced System Design                               |
| Site Reliability Engineering                          | Google SRE Team               | Reliability and Large-Scale Systems                  |
| The Site Reliability Workbook                         | Google SRE Team               | Practical SRE                                        |
| Database Internals                                    | Alex Petrov                   | Databases and Storage Systems                        |
| Fundamentals of Software Architecture                 | Mark Richards & Neal Ford     | Software Architecture                                |
| System Design on AWS                                  | Jayanth Kumar & Mandeep Singh | Cloud Architecture and Large-Scale Systems           |

---

## Important Topics

### 1. System Design Fundamentals

- Functional Requirements
- Non-Functional Requirements
- Scalability
- Availability
- Reliability
- Performance
- Latency
- Throughput
- Fault Tolerance
- Consistency
- CAP Theorem
- ACID
- Eventual Consistency

### 2. Networking

- HTTP / HTTPS
- TCP / UDP
- DNS
- IP Addresses
- Ports
- Load Balancers
- Reverse Proxy
- CDN
- WebSockets
- REST
- gRPC
- Network Latency

### 3. Databases

- SQL vs NoSQL
- Database Indexing
- Transactions
- Replication
- Sharding
- Partitioning
- Read Replicas
- Primary-Replica Architecture
- Database Consistency
- Distributed Databases

### 4. Caching

- Cache Fundamentals
- Cache-Aside
- Write-Through
- Write-Back
- Cache Invalidation
- Redis
- Memcached
- Distributed Caching
- Cache Eviction Policies

### 5. Distributed Systems

- Horizontal Scaling
- Vertical Scaling
- Service Discovery
- Distributed Transactions
- Consensus
- Leader Election
- Replication
- Partitioning
- Fault Tolerance
- Idempotency
- Eventual Consistency

### 6. Messaging & Event-Driven Architecture

- Message Queues
- Pub/Sub
- Kafka
- RabbitMQ
- Event Streaming
- Producers
- Consumers
- Consumer Groups
- Dead Letter Queues
- Retry Mechanisms

### 7. Microservices

- Monolith vs Microservices
- Service Boundaries
- API Gateway
- Service Discovery
- Inter-Service Communication
- Database per Service
- Distributed Transactions
- Circuit Breaker
- Rate Limiting

### 8. Storage

- Object Storage
- Block Storage
- File Storage
- Distributed File Systems
- Blob Storage
- Data Replication
- Data Partitioning

### 9. Reliability

- High Availability
- Fault Tolerance
- Disaster Recovery
- Backup Strategies
- Failover
- Graceful Degradation
- Circuit Breakers
- Retries
- Timeouts
- Health Checks

### 10. Observability

- Logging
- Metrics
- Tracing
- Monitoring
- Alerting
- SLIs
- SLOs
- SLAs
- Distributed Tracing

---

## Common System Design Components

| Component         | Purpose                              |
| ----------------- | ------------------------------------ |
| Load Balancer     | Distributes traffic across servers   |
| CDN               | Delivers content closer to users     |
| API Gateway       | Entry point for backend services     |
| Cache             | Reduces latency and database load    |
| Database          | Persistent data storage              |
| Message Queue     | Asynchronous communication           |
| Object Storage    | Stores files and large objects       |
| Search Engine     | Fast text and document search        |
| Service Discovery | Helps services locate each other     |
| Rate Limiter      | Controls request rates               |
| Reverse Proxy     | Routes and manages incoming requests |
| Monitoring System | Tracks system health and performance |

---

## Practice System Design Problems

Start with simpler systems and gradually increase complexity.

### Beginner

- URL Shortener
- Pastebin
- File Storage System
- Rate Limiter
- Web Crawler
- Notification System

### Intermediate

- Twitter / X
- Instagram
- YouTube
- WhatsApp
- Uber
- Food Delivery System
- Online Ticket Booking System
- E-commerce Platform

### Advanced

- Distributed Cache
- Distributed Message Queue
- Google Drive
- Netflix
- Distributed File Storage
- Search Engine
- Payment System
- Real-Time Location Tracking
- Distributed Job Scheduler
- Large-Scale Notification System

---

## System Design Interview Framework

When solving a system design problem, follow this general process:

```text
1. Clarify Requirements
        ↓
2. Define Functional Requirements
        ↓
3. Define Non-Functional Requirements
        ↓
4. Estimate Scale
        ↓
5. Define APIs
        ↓
6. Design High-Level Architecture
        ↓
7. Choose Databases
        ↓
8. Add Caching
        ↓
9. Add Load Balancing
        ↓
10. Add Queues / Asynchronous Processing
        ↓
11. Discuss Scalability
        ↓
12. Discuss Reliability & Fault Tolerance
        ↓
13. Identify Bottlenecks
        ↓
14. Improve the Architecture
```
