# Directus FinOps

Source: https://directus.com/pricing

## Cost Structure

Directus uses a tiered subscription model for cloud hosting, with the open-source self-hosted option available at no cost. Cloud plans add optional hosting on top of the software license.

### Plan Pricing Summary

| Plan | Monthly Cost (Annual) | Monthly Cost (Monthly) | Key Limits |
|------|----------------------|------------------------|------------|
| Core | $0 | $0 | 3 seats, 25 Collections, 5 Flows |
| Team | $499 | $599 | 10 SSO seats, 50 Collections, 20 Flows |
| Enterprise | Custom | Custom | 50+ seats, 200+ Collections, Unlimited Flows |
| Open Innovation Grant | $0 (self-hosted) / $99 (cloud) | — | Full features, eligibility required |
| Self-Hosted (OSS) | Free | Free | No limits |

### Cloud Hosting Add-On

- Cloud hosting is an optional add-on for the Core and Team plans at $99/month.
- Enterprise cloud pricing is custom and negotiated per deployment.

## Cost Optimization Strategies

### Self-Hosting
- The open-source Directus can be self-hosted at zero software cost on any infrastructure (Docker, VPS, Kubernetes).
- Teams comfortable managing infrastructure can run Directus on low-cost cloud VMs (e.g., a $6–$20/month VPS is sufficient for many small projects).
- Docker Compose deployment is the simplest approach and is well-documented.

### Plan Selection
- Start with the Core free plan for development, prototyping, or small teams under 3 users.
- Upgrade to Team only when SSO, more than 25 collections, or more than 5 automation flows are required.
- Negotiate Enterprise pricing with multi-year commitments or volume for discounts.

### Open Innovation Grant
- Organizations under $5M revenue and 50 employees can apply for the grant, which provides full-featured access at $0 (self-hosted) or $99/month (cloud).
- This dramatically reduces costs for eligible startups and non-profits.

## Billing Notes

- Annual billing for Team saves approximately $1,200/year ($499/month vs. $599/month).
- No per-API-call charges on any plan; cost is flat subscription-based.
- Enterprise agreements may include volume discounts, custom SLAs, and multi-year pricing.
- Non-profits, open-source projects, and academic institutions may qualify for additional discounts — contact Directus sales.

## Cost Visibility

- Cloud plans include usage dashboards in the Directus Cloud console.
- Self-hosted deployments can integrate with standard observability tooling (Prometheus, Grafana) to track request volume and infrastructure costs independently.
- No surprise overage charges on flat-rate subscription plans; feature limits are enforced rather than metered billing.

## Infrastructure Costs (Self-Hosted Reference)

| Deployment Size | Recommended Spec | Estimated Monthly Infrastructure Cost |
|----------------|-----------------|--------------------------------------|
| Development / Small | 1 vCPU, 1 GB RAM | $5–$15 (VPS) |
| Small Production | 2 vCPU, 4 GB RAM | $20–$60 (VPS/cloud VM) |
| Medium Production | 4 vCPU, 8 GB RAM | $60–$150 (cloud VM) |
| Large / HA | 8+ vCPU, 16+ GB RAM, load balancer | $200+ (varies by cloud provider) |

Note: Infrastructure costs above are estimates and depend on the chosen cloud provider, region, storage, and traffic volumes.
