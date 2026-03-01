# Cache patterns

## Cache-aside
App reads cache first; on miss reads DB and populates cache.

## Write-through
Writes go to cache and DB together.

## Write-behind
Writes go to cache, DB updated asynchronously.

## Refresh-ahead
Proactively refresh hot keys before TTL expires.

## Practice prompts
- Pick one pattern for a product catalog and justify.

## My notes
