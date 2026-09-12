# Database Architecture

PostgreSQL is the transactional system of record. Use UUID/ULID identifiers, UTC timestamps, explicit currencies, foreign keys, check constraints, and indexed organization scopes. Use JSONB only for provider payloads and evolving extraction metadata, not core relationships.

Object storage holds encrypted document binaries; PostgreSQL stores hashes, metadata, ACL references, and processing state. Search begins with PostgreSQL full-text/trigram indexes and may add a dedicated search engine when measured scale requires it. Analytics use read replicas or an ETL-fed warehouse, never long-running queries on the write primary.

Backups must be encrypted, regularly restored in a separate environment, and tested against the RPO/RTO targets.
