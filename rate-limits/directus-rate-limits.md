# Directus Rate Limits

Source: https://directus.com/docs/api, https://directus.com/pricing

## Cloud Hosting Rate Limits

Directus Cloud applies rate limits to protect the shared infrastructure. Specific numeric limits are not publicly documented per plan tier and are subject to change; contact Directus for exact quotas on Team and Enterprise cloud instances.

### Known Limits (Cloud)

- **Core Plan:** Shared cloud infrastructure; rate limiting applied at the platform level to ensure fair use across all tenants.
- **Team Plan:** Higher throughput than Core; specific request/minute limits are available on request from Directus support.
- **Enterprise Plan:** Custom rate limits negotiated as part of the enterprise agreement; dedicated infrastructure options available.

## Self-Hosted Rate Limits

Directus does not apply built-in rate limits in the open-source self-hosted deployment by default. Organizations are expected to implement rate limiting at the infrastructure layer:

- **Reverse Proxy:** Configure rate limiting via nginx, Caddy, or Traefik in front of the Directus instance.
- **Load Balancer:** Apply per-IP or per-token rate limiting at the load balancer (e.g., AWS ALB, Cloudflare, etc.).
- **API Gateway:** Route Directus behind an API gateway (Kong, Tyk, AWS API Gateway) for fine-grained rate limit policies.

## API Request Behavior

- **Authentication:** Unauthenticated requests are limited to public collections only; authenticated requests use the token's associated role and permissions.
- **Timeouts:** Long-running queries may time out depending on server configuration; default Node.js process limits apply.
- **Pagination:** The `limit` parameter defaults to 100 items; maximum configurable limit is controlled by the `MAX_PAYLOAD_SIZE` environment variable on self-hosted instances.

## Rate Limit Headers

When rate limiting is enforced (e.g., behind a gateway), standard HTTP rate limit headers are returned:

| Header | Description |
|--------|-------------|
| `X-RateLimit-Limit` | Maximum requests allowed in the time window |
| `X-RateLimit-Remaining` | Requests remaining in the current window |
| `X-RateLimit-Reset` | Unix timestamp when the window resets |
| `Retry-After` | Seconds to wait after a 429 response |

## Error Responses

- **429 Too Many Requests:** Returned when rate limits are exceeded.
- **503 Service Unavailable:** May be returned under extreme load on cloud instances.
