# Performance

Define workload profiles before implementation: portfolio dashboard reads, resident conversations, work-order updates, document ingestion, payment callbacks, and analytics exports. Load-test realistic tenant distributions and large portfolios, not only averages.

Priorities are indexed scoped queries, cursor pagination, bounded payloads, asynchronous provider work, connection-pool limits, read models for dashboards, batch imports, and backpressure. Track p50/p95/p99 latency, throughput, queue age, database saturation, cache hit rate, and AI/provider latency and cost.

Performance budgets are hypotheses until measured in staging with production-like data and redacted document sizes.
