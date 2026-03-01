# Failover patterns

## What it is
Redirect traffic from a failed component to a healthy one (same region or another region).

## Gotchas
- Health checks can lie (partial failures).
- Failover can create thundering herds.

## Practice prompts
- Design health checks for a stateless API service and for a DB.

## My notes
