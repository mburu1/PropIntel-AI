# Testing Strategy

- **Unit:** domain invariants, value objects, policies, state transitions.
- **Application:** authorization, transactions, idempotency, outbox behavior.
- **Integration:** PostgreSQL, Redis, broker, object storage, and provider adapters using disposable infrastructure.
- **Contract:** OpenAPI compatibility and event-schema consumer/provider tests.
- **Security:** tenant isolation, object authorization, webhook signatures, injection, secrets, and dependency checks.
- **Workflow/E2E:** lease, request-to-work-order, document extraction review, invoicing/payment/reconciliation.
- **AI evaluation:** groundedness, citation correctness, refusal behavior, sensitive-data leakage, latency, and cost on versioned datasets.

Every defect gets a regression test. Tests must be deterministic, parallelizable, and safe to rerun.
