# Directus

Directus is an open-source data platform that wraps any SQL database with a REST and GraphQL API, auto-generated from the schema, plus a no-code admin app for data management. It supports PostgreSQL, MySQL, SQLite, MS SQL, OracleDB, and CockroachDB, and can be deployed as a self-hosted open-source project or via Directus Cloud.

## Links

- **Website:** https://directus.com/
- **Documentation:** https://directus.com/docs
- **API Reference:** https://directus.com/docs/api
- **GraphQL Docs:** https://directus.com/docs/graphql
- **Pricing:** https://directus.com/pricing
- **GitHub Organization:** https://github.com/directus
- **GitHub Repository:** https://github.com/directus/directus
- **LinkedIn:** https://www.linkedin.com/company/directus-io
- **Blog:** https://directus.com/blog
- **Community Forum:** https://community.directus.io
- **Discord:** https://discord.com/invite/directus
- **Live Sandbox:** https://sandbox.directus.io

## About

Directus provides an instant REST and GraphQL API layer on top of any SQL database without altering the underlying schema. Key platform capabilities include:

- **REST and GraphQL APIs:** Auto-generated, schema-driven APIs with full CRUD, filtering, sorting, pagination, and nested relational queries.
- **Visual Data Studio:** No-code interface for non-technical users to manage database content.
- **Policy-Based Access Control:** Granular RBAC with role-based and attribute-based policies.
- **Automation Engine (Flows):** Visual low-code workflow builder for event-driven automation.
- **Built-in AI Assistant:** Integrated AI capabilities including translations and data insights.
- **Digital Asset Management:** File upload, storage, and transformation pipeline.
- **Real-Time and WebSockets:** Live data subscriptions via WebSocket connections.
- **MCP Server:** Model Context Protocol server for integration with AI agents (Claude, ChatGPT, Cursor).
- **Extensibility:** Custom extensions for endpoints, hooks, interfaces, displays, panels, and modules.

## Repository Structure

```
directus/
├── apis.yml                          # APIs.json catalog entry
├── README.md                         # This file
├── graphql/
│   └── directus-graphql.md           # GraphQL API documentation
├── plans/
│   └── directus-plans.md             # Pricing plan details
├── rate-limits/
│   └── directus-rate-limits.md       # Rate limiting information
└── finops/
    └── directus-finops.md            # Cost structure and optimization
```

## APIs

| API | Type | Description |
|-----|------|-------------|
| Directus REST API | REST | Auto-generated CRUD API over any SQL database |
| Directus GraphQL API | GraphQL | Schema-driven GraphQL with queries, mutations, and subscriptions |
