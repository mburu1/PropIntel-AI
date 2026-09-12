# Messaging

Use an outbox/inbox pattern with a durable broker. Events are facts, named in past tense, versioned, and carry `eventId`, `eventType`, `occurredAt`, `organizationId`, `aggregateId`, `aggregateVersion`, `correlationId`, and `causationId`.

Important events include `LeaseActivated`, `RequestCreated`, `WorkOrderCompleted`, `DocumentExtractionCompleted`, `InvoiceIssued`, `PaymentSucceeded`, and `RecommendationApproved`.

Delivery is at least once. Consumers must be idempotent, retry transient failures with backoff, quarantine poison messages in a dead-letter queue, and expose lag and failure metrics. Ordering is guaranteed per aggregate where required, not globally.
