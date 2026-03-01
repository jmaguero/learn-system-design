# Circuit breaker

## Intent
Stop calling a dependency that is failing to prevent cascading failures.

## How it works
Closed → Open → Half-open state machine; observe error rates and timeouts.

## Practice prompts
- What metrics would trigger opening the breaker?

## My notes
