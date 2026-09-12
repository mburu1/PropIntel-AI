# Observability

Instrument API requests, database calls, broker publishing/consumption, provider calls, document pipelines, and AI retrieval/generation with OpenTelemetry.

Logs are structured and contain correlation identifiers, actor type, organization scope, outcome, and latency, but no raw secrets or unnecessary personal data. Metrics cover availability, latency, error rate, queue lag, workflow SLA, payment reconciliation, extraction confidence, token/cost usage, and cache hit rate. Traces connect synchronous requests to asynchronous jobs.

Alerts should be actionable: API SLO burn, failed payments, stuck documents, dead letters, tenant-isolation errors, backup failures, and provider degradation. Define runbooks and retention per data classification.
