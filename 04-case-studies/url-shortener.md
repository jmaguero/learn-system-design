# 🔗 Design a URL Shortener (e.g., bit.ly)

## Requirements

### Functional
- Given a long URL, generate a short URL
- Redirect short URL to original
- (Optional) Custom aliases, expiration, analytics

### Non-Functional
- High availability (99.99% uptime)
- Low latency redirects (<10ms)
- Scale: 100M URLs created/day, 10B redirects/day

## Estimation
- Write QPS: ~1,200/s
- Read QPS: ~115,000/s (read-heavy)
- Storage: 100M * 500 bytes = 50GB/day

## High-Level Design

```
Client → Load Balancer → App Servers → Cache (Redis)
                                     ↓ (cache miss)
                                  Database (SQL/NoSQL)
```

## Short URL Generation
- **Hashing**: MD5/SHA256 → take first 7 chars (collision risk)
- **Base62 Encoding**: Encode an auto-incremented ID (a-z, A-Z, 0-9)
  - 7 chars of base62 = 62^7 = ~3.5 trillion URLs
- **Random UUID**: Simple, but check for collisions

## Database Schema
```sql
CREATE TABLE urls (
  id BIGINT PRIMARY KEY,
  short_code VARCHAR(10) UNIQUE,
  long_url TEXT NOT NULL,
  created_at TIMESTAMP,
  expires_at TIMESTAMP
);
```

## Trade-offs
- SQL vs NoSQL: NoSQL (Cassandra/DynamoDB) better for extreme scale
- Caching: Cache popular short codes in Redis (LRU)
- Redirect: HTTP 301 (permanent, cached) vs 302 (temporary, trackable)

## Notes

> Add your own diagrams and notes here.
