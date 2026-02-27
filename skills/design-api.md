---
name: design-api
description: Design a REST or GraphQL API from requirements
parameters:
  - name: feature
    description: The feature or domain to design an API for
    required: true
  - name: style
    description: API style (REST or GraphQL)
    required: false
    default: REST
  - name: auth
    description: Authentication method (JWT, API key, OAuth2, session)
    required: false
    default: JWT
---

# Design API

Design a complete {{style}} API for "{{feature}}".

## Steps

1. Identify resources and operations (CRUD + custom actions)
2. Define endpoint structure with HTTP methods and paths
3. Design request/response schemas as TypeScript types
4. Plan authentication ({{auth}}) and authorization
5. Define error response format
6. Add pagination, filtering, and sorting where applicable
7. Document rate limiting strategy

## Output Format

### Endpoints Table
| Method | Path | Description | Auth |
|--------|------|-------------|------|

### TypeScript Types
```typescript
// Request and response types for each endpoint
```

### Error Handling
Standard error envelope with codes, messages, and details.

### Rate Limits
Per-endpoint rate limit recommendations based on expected usage.
