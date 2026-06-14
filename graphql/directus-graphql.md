# Directus GraphQL API

Auto-generated GraphQL API that mirrors the REST API surface, providing strongly-typed queries and mutations for all collections and system endpoints in a connected SQL database.

**Endpoint:** `https://your-directus-instance/graphql`

**System Endpoint:** `https://your-directus-instance/graphql/system`

**Documentation:** https://directus.com/docs/graphql

## Authentication

Requests are authenticated via a Bearer token passed in the `Authorization` header:

```
Authorization: Bearer <access_token>
```

Tokens are obtained via the `/auth/login` REST endpoint or the `auth_login` mutation.

## Key Capabilities

- **Queries:** Read items from any collection with filtering, sorting, pagination, and field selection.
- **Mutations:** Create, update, delete, and upsert items in any collection.
- **Aggregations:** Count, sum, avg, min, max, and count distinct per collection.
- **Nested Relations:** Traverse relational data (Many-to-One, One-to-Many, Many-to-Many) in a single query.
- **Subscriptions:** Real-time data updates via WebSocket connection.
- **System Endpoints:** Manage users, roles, permissions, fields, collections, and files via the `/graphql/system` endpoint.

## Filtering

Directus GraphQL supports a rich filter object using logical operators (`_and`, `_or`) and field-level comparisons (`_eq`, `_neq`, `_lt`, `_lte`, `_gt`, `_gte`, `_in`, `_nin`, `_contains`, `_starts_with`, `_ends_with`, etc.).

## Schema

A full SDL schema covering all system types, queries, mutations, subscriptions, filter operators, aggregations, and input types is available in [directus-schema.graphql](directus-schema.graphql). It was derived from the Directus open-source codebase at `api/src/services/graphql/`.

## References

- Documentation: https://directus.com/docs/graphql
- API Reference: https://directus.com/docs/api
- GitHub Repository: https://github.com/directus/directus
- Schema Source: https://github.com/directus/directus/tree/main/api/src/services/graphql
