# Bulkhead

## Intent
Isolate resources so failure/overload in one area doesn’t sink the entire service.

## Examples
Separate thread pools per dependency; isolate tenants; isolate queues.

## Practice prompts
- Where would you put bulkheads in a payment service?

## My notes
