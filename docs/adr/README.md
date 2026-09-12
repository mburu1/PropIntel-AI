# Architecture Decision Records

ADRs record context, decision, alternatives, consequences, and status. Proposed initial decisions:

1. **ADR-001: Start with a modular monolith** — reduce distributed-systems overhead while boundaries are learned.
2. **ADR-002: PostgreSQL as transactional source of truth** — strong consistency and mature relational querying.
3. **ADR-003: Outbox plus durable broker** — reliable asynchronous integration without dual-write loss.
4. **ADR-004: Human approval for consequential AI actions** — preserve accountability and reduce automation harm.

New decisions should be added as `ADR-NNN-short-title.md` in this directory.
