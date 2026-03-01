# CAP theorem

## Model
CAP says that under a network partition you must choose between:
- Consistency: reads see the latest write.
- Availability: every request gets a response.
- Partition tolerance: the system keeps operating despite splits.

## Practical takeaway
Treat partitions as inevitable; decide whether to degrade by rejecting requests (CP) or serving possibly-stale data (AP).

## Practice prompts
- Pick a product (chat, feed, payments) and justify AP vs CP.

## My notes
