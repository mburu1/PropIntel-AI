# PropIntel AI

AI-native real-estate intelligence and property operations platform.

PropIntel AI brings property portfolios, leases, tenants, maintenance, documents, payments, analytics, and predictive decision support into one operational system. It is designed for property managers, owners, operators, finance teams, leasing teams, maintenance coordinators, and tenants.

> **Status:** Product and architecture specification only. No application code has been implemented yet.

## Product promise

- **One operational record:** properties, units, parties, leases, work orders, documents, and payments share consistent identities.
- **Decision support, not opaque automation:** AI recommendations cite source data, expose confidence, and require human approval for consequential actions.
- **Operational continuity:** asynchronous work, retries, audit trails, and graceful degradation are first-class requirements.
- **Tenant-friendly interactions:** conversations, requests, notices, and payment journeys are available through secure digital channels.

## Documentation map

| Concern | Document |
|---|---|
| Problem and product requirements | [`docs/problem-requirements/`](./docs/problem-requirements/) |
| Object-oriented analysis and design | [`docs/ooad/`](./docs/ooad/) |
| UML diagrams | [`docs/uml/`](./docs/uml/) |
| System architecture | [`docs/architecture/`](./docs/architecture/) |
| Domain model | [`docs/domain-model/`](./docs/domain-model/) |
| Entity relationship design | [`docs/erd/`](./docs/erd/) |
| Database architecture | [`docs/database-architecture/`](./docs/database-architecture/) |
| API contracts | [`docs/api-contracts/`](./docs/api-contracts/) |
| Security model | [`docs/security-model/`](./docs/security-model/) |
| Messaging and events | [`docs/messaging/`](./docs/messaging/) |
| Caching strategy | [`docs/caching/`](./docs/caching/) |
| Observability | [`docs/observability/`](./docs/observability/) |
| Testing strategy | [`docs/testing-strategy/`](./docs/testing-strategy/) |
| CI/CD | [`docs/ci-cd/`](./docs/ci-cd/) |
| Docker and local infrastructure | [`docs/docker/`](./docs/docker/) |
| Deployment | [`docs/deployment/`](./docs/deployment/) |
| Architecture decision records | [`docs/adr/`](./docs/adr/) |
| Trade-offs | [`docs/trade-offs/`](./docs/trade-offs/) |
| Performance | [`docs/performance/`](./docs/performance/) |
| Limitations and risks | [`docs/limitations/`](./docs/limitations/) |

## Proposed bounded contexts

1. **Portfolio:** organizations, properties, buildings, units, ownership, occupancy.
2. **Leasing:** listings, applications, leases, renewals, notices.
3. **Resident experience:** tenant profiles, conversations, requests, communications.
4. **Property operations:** inspections, work orders, vendors, preventive maintenance.
5. **Documents:** ingestion, OCR, classification, extraction, versioning, retention.
6. **Finance:** charges, invoices, payments, refunds, reconciliation.
7. **Intelligence:** metrics, forecasts, anomaly detection, recommendations, AI evidence.
8. **Platform:** identity, authorization, audit, notifications, integrations, configuration.

## Initial non-functional targets

- Tenant-facing API availability: **99.9% monthly**, excluding planned maintenance.
- Read API p95 latency: **<300 ms** for normal portfolio queries.
- Command API p95 latency: **<700 ms** when no external provider is synchronously called.
- Event processing: at-least-once delivery with idempotent consumers.
- Financial and authorization changes: immutable audit record and explicit actor.
- Recovery objectives: **RPO ≤15 minutes**, **RTO ≤60 minutes** for the first production tier.

## Guiding principles

- Modular monolith first; extract services only when ownership, scale, or isolation justifies it.
- PostgreSQL is the system of record; object storage holds binary documents.
- OpenAPI and event schemas are versioned contracts.
- AI outputs are advisory by default, grounded in tenant-authorized data, and traceable.
- Privacy, accessibility, and regional data-residency requirements are designed in rather than bolted on.

## Current repository state

There is no runtime, package manifest, schema, or test suite yet. The existing [`docker-compose.yml`](./docker-compose.yml) is retained as an infrastructure placeholder and should be updated when implementation begins.

## Suggested implementation sequence

1. Confirm personas, geography, regulatory obligations, and MVP boundaries.
2. Implement identity, organizations, portfolio, units, and audit foundations.
3. Add leasing and resident requests.
4. Add work orders, documents, and finance integrations.
5. Add analytics and grounded AI workflows after reliable operational data exists.
6. Validate with pilot customers before decomposing modules into independently deployed services.

## License

See [`LICENSE`](./LICENSE).
