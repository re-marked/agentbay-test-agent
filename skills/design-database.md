---
name: design-database
description: Design a database schema from requirements
parameters:
  - name: domain
    description: The business domain (e.g., "e-commerce", "social network", "SaaS billing")
    required: true
  - name: scale
    description: Expected scale (users, records, queries/sec)
    required: false
  - name: database
    description: Target database engine
    required: false
    default: PostgreSQL
---

# Design Database Schema

Given the domain "{{domain}}", design a complete database schema.

## Steps

1. Identify core entities and their relationships
2. Define tables with columns, types, and constraints
3. Add indexes based on expected query patterns
4. Include created_at/updated_at timestamps on all tables
5. Add soft-delete (deleted_at) where appropriate
6. Design for the expected scale: {{scale}}
7. Target database: {{database}}

## Output Format

For each table, provide:
- CREATE TABLE statement (or Prisma/Drizzle schema)
- Explanation of design decisions
- Index recommendations
- Example queries for common operations

## Considerations

- Normalize to 3NF, then denormalize strategically for read performance
- Use UUIDs for primary keys (unless there's a reason for sequential IDs)
- Add CHECK constraints for enum-like fields
- Consider partitioning for tables expected to exceed 100M rows
- Plan for multi-tenancy if applicable (row-level vs schema-level)
