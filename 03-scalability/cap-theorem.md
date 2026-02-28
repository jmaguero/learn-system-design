# ⚖️ CAP Theorem

## Definition
In a distributed system, you can only guarantee **two of three** properties:

- **C**onsistency — Every read receives the most recent write
- **A**vailability — Every request receives a response (not necessarily latest data)
- **P**artition Tolerance — System continues operating despite network partitions

> 🔑 **Network partitions always happen**, so you must choose between C and A.

## CA vs CP vs AP

| Type | Systems | Trade-off |
|---|---|---|
| CP | HBase, Zookeeper, MongoDB | Sacrifices availability during partition |
| AP | Cassandra, DynamoDB, CouchDB | May return stale data |
| CA | Traditional RDBMS (single node) | Not truly distributed |

## PACELC Extension
PAC**ELC** extends CAP: even without partition (**E**lse), there's a trade-off between **L**atency and **C**onsistency.

## Notes

> Add your personal notes here.
