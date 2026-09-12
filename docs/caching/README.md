# Caching

Redis is an acceleration layer, never the source of truth. Cache authorized, non-sensitive reads such as property summaries, permissions, and dashboard aggregates with bounded TTLs and organization-aware keys.

Invalidate by domain event where correctness matters; use stale-while-revalidate for dashboards. Do not cache payment state, authorization decisions beyond a short controlled TTL, or document contents without explicit encryption and access controls. Every cache path needs a database fallback and stampede protection.
