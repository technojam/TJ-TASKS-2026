# System Design Tasks - 2026

Welcome to Team TechnoJam Auditions 2026!!!!!!

We have prepared 3 System Design tasks according to their respective difficulty levels.

> **Resources:** For reference materials, tools, and helpful links for system design, check out `resources.md`.

Note: Complete and submit the assigned task according to the instructions provided by the TechnoJam team.

---

## Easy - Flash Sale & Inventory Management System

### Task: High-Traffic Checkout & Inventory Control

Design a high-traffic e-commerce flash sale system where thousands of users attempt to purchase a limited number of products at exactly the same time. The system must prevent overselling while remaining responsive during extreme traffic spikes.

### Requirements

- Support 2 million users during peak traffic.
- Handle 50,000+ requests per second during the sale.
- Maintain accurate inventory and prevent overselling.
- Prevent duplicate orders.
- Support cart and checkout workflows.
- Handle payment failures and order expiration.
- Provide real-time inventory updates.
- Protect APIs from abuse and bots.
- Recover from partial service failures.
- Deliver: high-level architecture, checkout flow, database schema, inventory reservation strategy, concurrency control, caching strategy, rate limiting strategy, queue/event architecture, API design, failure/rollback strategy, monitoring, and load testing strategy.

### Bonus

Design a mechanism that allows users to join a virtual waiting room before the sale begins.

### Resources

- Redis Lua scripting (atomic inventory decrement): https://redis.io/docs/latest/develop/interact/programmability/eval-intro/
- Rate limiting patterns: https://cloud.google.com/architecture/rate-limiting-strategies-techniques

---

## Medium - Global Food Delivery Platform

### Task: Real-Time Order, Matching and Delivery System

Design a global food delivery platform that connects customers, restaurants, and delivery partners in real time. The system must handle millions of concurrent users while coordinating highly dynamic delivery operations, and every step of the order lifecycle can fail independently.

### Requirements

- 50 million daily active users, 5 million orders per day.
- 500,000+ concurrent delivery partners with real-time location tracking.
- Restaurant availability management and dynamic delivery partner assignment.
- ETA calculation, payment processing, cancellations, and refunds.
- Surge pricing and a notification system.
- Multi-region deployment with high availability.
- Deliver: global architecture, order lifecycle design, delivery partner matching system, real-time location architecture, event-driven order processing, database and caching architecture, payment and notification architecture, failure recovery, multi-region strategy, observability, and disaster recovery strategy.

### Bonus

Design a dynamic delivery-partner allocation algorithm considering distance, traffic, delivery time, partner availability, order priority, and current workload.

### Resources

- Geospatial indexing (Uber H3): https://h3geo.org/
- Event-driven architecture with Kafka: https://kafka.apache.org/documentation/
- Designing data-intensive applications (consistency & event-driven systems reference): https://dataintensive.net/

---

## Hard - Multi-Region Digital Payment Platform

### Task: Consistent, Idempotent Global Payments System

Design a global digital payment platform capable of processing millions of transactions while maintaining correctness, security, availability, and a complete audit trail. The system must **never process the same payment twice or lose a confirmed transaction.**

### Requirements

- 100 million registered users, 10 million transactions per hour.
- Multi-region deployment with strong consistency for account balances.
- Idempotent transactions and duplicate transaction prevention.
- Handle payment provider failures with automatic retries.
- Complete audit history and fraud detection.
- Encryption, authentication, and authorization.
- Disaster recovery and regulatory compliance.
- Deliver: complete architecture, transaction lifecycle, ledger/database design, consistency model, idempotency strategy, distributed transaction strategy, payment provider integration, retry and dead-letter queue strategy, fraud detection architecture, security architecture, audit logging, multi-region architecture, disaster recovery plan, and failure scenario analysis.

### Mandatory Failure Scenarios

Explain what happens if:

1. The payment succeeds but your database is unavailable.
2. The database transaction succeeds but the API crashes before responding.
3. A payment provider sends the same webhook multiple times.
4. Two requests attempt to spend the same balance.
5. An entire region becomes unavailable.
6. A message is delivered twice.
7. A message is lost.
8. A service becomes extremely slow instead of completely failing.

### Bonus

Design a mechanism for detecting suspicious transactions in real time without significantly increasing payment latency.

### Resources

- Idempotency keys in payment systems (Stripe docs): https://stripe.com/docs/api/idempotent_requests
- Saga pattern for distributed transactions: https://microservices.io/patterns/data/saga.html
- Google Spanner consistency model (reference for strong consistency at scale): https://cloud.google.com/spanner/docs/true-time-external-consistency

---

## Submission Requirements

- System architecture (high-level + detailed, data flow, service interactions)
- Database design (ER diagram, schema, indexing, replication strategy)
- API design (endpoints, request/response structure, auth, rate limiting, idempotency)
- Scalability analysis (traffic estimates, storage, bottlenecks, capacity planning)
- Failure analysis (minimum 5 documented failure scenarios per task)
- Security design (authN/authZ, encryption, secrets management, abuse prevention)
- Observability plan (metrics, logs, tracing, alerts, SLOs/SLIs)
- Disaster recovery plan (RTO, RPO, backup and recovery strategy)
- Diagrams and documentation

> **Note:** These tasks are evaluated as well-reasoned architecture documents, not live implementations. As written (with the deliverables being docs, diagrams, and failure analysis — not live systems), they're reasonable - a working prototype is optional unless explicitly required for the selected task.

Make sure your work is properly documented and that you understand the trade-offs behind every architectural decision.

Good Luck!

**Team TechnoJam**
