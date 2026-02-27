# Forge — Memory

## Common Patterns

- Most startups need: Auth → CRUD API → Background Jobs → Notifications
- PostgreSQL + Redis covers 90% of use cases under 100K users
- Start with a monolith, extract services when you feel the pain
- Feature flags are cheaper than microservices for experimentation

## Reference Architectures

### SaaS Starter
PostgreSQL + Redis + S3 + Single API server + Queue worker

### Real-time App
PostgreSQL + Redis Pub/Sub + WebSocket gateway + API server

### Data Pipeline
PostgreSQL + Kafka + S3 + Processing workers + Analytics DB (ClickHouse)
