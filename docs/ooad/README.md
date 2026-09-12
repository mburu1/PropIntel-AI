# OOAD

The design uses domain-driven object-oriented analysis. Aggregates protect invariants; application services coordinate use cases; repositories abstract persistence; domain events communicate completed facts.

## Core aggregates

| Aggregate | Invariants |
|---|---|
| Property | A unit belongs to one property/building hierarchy. |
| Lease | Parties, dates, status, and charges form a valid tenancy agreement. |
| WorkOrder | Status transitions are ordered and assignment is explicit. |
| Document | Versions are immutable; extraction is linked to a source version. |
| Payment | Provider callbacks are idempotent and amounts/currency cannot be changed after capture. |
| Recommendation | Evidence, model version, confidence, and approval state are recorded. |

## Use-case pattern

`Controller -> Application service -> Aggregate/repository -> Domain events -> Outbox publisher`

Commands validate intent and authorization. Queries use read models and never mutate aggregates. External providers are accessed through ports and adapters.
