# ERD

```mermaid
erDiagram
  ORGANIZATION ||--o{ PROPERTY : owns
  PROPERTY ||--o{ UNIT : contains
  UNIT ||--o{ LEASE_UNIT : included_in
  LEASE ||--o{ LEASE_UNIT : covers
  PARTY ||--o{ LEASE_PARTY : signs
  LEASE ||--o{ LEASE_PARTY : has
  UNIT ||--o{ REQUEST : receives
  REQUEST ||--o{ WORK_ORDER : becomes
  VENDOR ||--o{ WORK_ORDER : performs
  ENTITY ||--o{ DOCUMENT : has
  INVOICE ||--o{ PAYMENT : settled_by
  ORGANIZATION ||--o{ USER_MEMBERSHIP : grants
```

All business tables include a stable identifier, organization scope where applicable, created/updated timestamps, and optimistic-concurrency metadata. Financial records are append-oriented; corrections use reversals rather than destructive edits.
