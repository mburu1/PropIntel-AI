# CI/CD

Pull requests should run formatting, linting, type checks, unit tests, integration tests, contract checks, dependency and secret scans, migration validation, and container builds. Main-branch pipelines publish immutable artifacts and attach SBOMs.

Promotion uses dev -> staging -> production with environment-specific configuration, approval gates for production, database migration safeguards, smoke tests, and automatic rollback or roll-forward procedures. Build provenance, artifact signing, and least-privilege deployment identities are required before production.
