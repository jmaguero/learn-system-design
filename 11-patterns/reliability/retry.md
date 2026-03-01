# Retry (with backoff and jitter)

## Intent
Recover from transient failures without amplifying load.

## Rules of thumb
Bound retries; use exponential backoff; add jitter; coordinate with timeouts; ensure idempotency.

## Practice prompts
- Explain why retries can cause outages.

## My notes
