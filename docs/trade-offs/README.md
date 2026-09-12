# Trade-offs

| Choice | Benefit | Cost / mitigation |
|---|---|---|
| Modular monolith first | Faster delivery and transactions | Requires strict boundaries and later extraction discipline |
| PostgreSQL plus read models | Strong writes and flexible queries | Projection lag; show freshness timestamps |
| At-least-once events | Reliable delivery | Duplicate handling; enforce idempotency |
| Managed AI providers | Faster capability and model choice | Cost, privacy, and vendor dependence; abstraction and controls |
| Human-in-the-loop AI | Safer high-impact decisions | Slower throughput; automate only low-risk actions |
| Shared platform with scoped tenants | Lower operational cost | Isolation risk; test authorization continuously |
