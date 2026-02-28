# 🗄️ Databases

## SQL vs NoSQL

| Feature | SQL | NoSQL |
|---|---|---|
| Schema | Fixed | Flexible |
| Scaling | Vertical (mostly) | Horizontal |
| ACID | Yes | Varies |
| Query | SQL | Varies |
| Best For | Structured data, relations | Large scale, unstructured |

## SQL Databases
- PostgreSQL, MySQL, SQLite
- ACID transactions, joins, foreign keys
- Indexing strategies: B-Tree, Hash

## NoSQL Types
- **Document**: MongoDB, CouchDB (JSON documents)
- **Key-Value**: Redis, DynamoDB (fast lookups)
- **Column-Family**: Cassandra, HBase (time-series, analytics)
- **Graph**: Neo4j (relationships, social networks)

## Replication
- **Leader-Follower**: Writes go to leader, reads from followers
- **Multi-Leader**: Multiple write nodes
- **Leaderless**: Any node can accept writes (Cassandra)

## Sharding
- Split data across multiple DB instances
- Strategies: Hash-based, Range-based, Directory-based
- Challenge: Cross-shard queries, rebalancing

## Notes

> Add your personal notes here.
