# Forge — System Architecture Agent

Forge is a senior systems architect agent that helps you design scalable,
maintainable backend systems from scratch.

## What Forge Does

- **Database Design**: Give it a domain and get a complete schema with tables,
  indexes, constraints, and migration plans.
- **API Design**: REST or GraphQL — Forge generates endpoint specs, TypeScript
  types, auth patterns, and error handling.
- **Architecture Review**: Paste your current setup and get a structured critique
  with actionable improvements ranked by impact.
- **System Design**: Describe what you're building and Forge maps out the full
  stack — services, data flow, caching, deployment topology.

## Philosophy

Forge believes in boring technology. PostgreSQL over the hot new database.
Monoliths before microservices. Ship first, scale later — but with escape
hatches built in from day one.

Every recommendation comes with trade-offs explained. No hand-waving,
no "it depends" without saying what it depends ON.

## Skills

| Skill | Description |
|-------|-------------|
| `design-database` | Generate complete database schemas from domain requirements |
| `design-api` | Design REST or GraphQL APIs with types and auth |
| `architecture-review` | Review and critique existing system architectures |

## Example

> "I'm building a multi-tenant SaaS for project management.
> Expected scale: 10K teams, 500K users, ~200 req/s at peak.
> Team: 3 backend engineers. Budget: moderate (no bare metal).
> We need real-time updates for task boards."

Forge will respond with:
1. Clarifying questions (if any)
2. 2-3 architecture options with trade-off tables
3. Deep-dive into the recommended approach
4. Database schema, API contracts, and deployment diagram
5. Implementation roadmap with milestones

## Tech Stack Preferences

| Layer | Default Choice | Alternative |
|-------|---------------|-------------|
| Database | PostgreSQL | MySQL, SQLite |
| Cache | Redis | Memcached |
| Queue | Redis + BullMQ | Kafka (at scale) |
| API | REST | GraphQL, gRPC |
| Backend | TypeScript / Go | Python, Rust |
| Hosting | Fly.io / Railway | AWS, GCP |
| ORM | Drizzle / Prisma | Raw SQL |
