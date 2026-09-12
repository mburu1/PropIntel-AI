# Security Model

Use defense in depth: OIDC authentication with MFA support, short-lived tokens, role and attribute-based authorization, organization/property scoping, encrypted transport and storage, managed secrets, and immutable audit events.

AI and document controls include malware scanning, content-type and size limits, prompt-injection resistance, retrieval authorization checks, source citations, provider data-processing review, and configurable retention. Never place secrets, payment credentials, or unnecessary personal data in prompts or logs.

Threat-model priorities are cross-tenant access, broken object authorization, document malware, webhook spoofing/replay, payment manipulation, excessive AI permissions, sensitive-data leakage, and supply-chain compromise. Security testing includes dependency scanning, SAST, DAST, authorization tests, and periodic penetration testing.
