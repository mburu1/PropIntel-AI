# Deployment

Deploy stateless API and worker workloads behind a managed ingress with private data services, centralized secrets, autoscaling, and network egress controls. Use managed PostgreSQL, Redis, object storage, broker, identity, and observability where practical.

Release steps: validate migrations -> deploy compatible application -> migrate/expand -> smoke test -> observe -> contract/feature cleanup. Document rollback limits for irreversible migrations and provider-side changes. Disaster recovery requires cross-zone resilience, encrypted backups, restore drills, and tested failover.
