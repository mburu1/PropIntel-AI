# Domain Model

## Principal entities

Organization owns portfolios and controls tenant isolation. A Property contains Buildings and Units. Parties may be people or companies with organization-scoped roles. A Lease connects one or more parties to one or more units for a period. Requests become WorkOrders, which may involve Vendors. Documents attach to any supported entity. Charges produce Invoices; Payments settle invoices. Insights and Recommendations reference metrics and source evidence.

## Key value objects

`Address`, `Money`, `DateRange`, `ContactPoint`, `Permission`, `SlaPolicy`, `ConfidenceScore`, and `DocumentHash`.

## State machines

- Lease: `Draft -> PendingSignature -> Active -> Expired | Terminated`
- Request: `New -> Acknowledged -> InProgress -> Resolved -> Closed`
- Work order: `Open -> Assigned -> Scheduled -> Completed -> Cancelled`
- Payment: `Initiated -> Pending -> Succeeded | Failed | Refunded`
- Document processing: `Uploaded -> Scanning -> Extracting -> ReviewRequired -> Approved | Rejected`
