# API Contracts

Use versioned REST/JSON contracts under `/api/v1`; publish OpenAPI as the source of truth. Use RFC 9457-style problem details for errors.

## Resource examples

| Method | Path | Purpose |
|---|---|---|
| GET | `/api/v1/properties` | List authorized properties |
| POST | `/api/v1/work-orders` | Create a work order |
| GET | `/api/v1/leases/{leaseId}` | Read a lease |
| POST | `/api/v1/documents` | Create an upload session |
| POST | `/api/v1/invoices/{invoiceId}/payments` | Start a payment |
| GET | `/api/v1/insights/portfolio` | Read portfolio intelligence |

Commands accept an `Idempotency-Key`; mutation responses return a resource identifier, version, and correlation ID. Pagination uses opaque cursors. Breaking changes require a new API version and a deprecation window.
