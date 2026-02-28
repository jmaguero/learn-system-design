# ⚡ Caching

## Why Cache?
- Reduce latency
- Decrease database load
- Improve throughput

## Cache Strategies

### Cache-Aside (Lazy Loading)
1. App checks cache
2. On miss → fetch from DB → store in cache
3. Most common pattern

### Write-Through
- Write to cache AND DB simultaneously
- Consistent but adds write latency

### Write-Behind (Write-Back)
- Write to cache first, async write to DB
- Fast writes, risk of data loss

### Read-Through
- Cache sits in front of DB
- Cache handles DB reads automatically

## Cache Eviction Policies
- **LRU** (Least Recently Used) — most common
- **LFU** (Least Frequently Used)
- **FIFO** (First In, First Out)
- **TTL** (Time To Live)

## Tools
- **Redis**: In-memory, supports data structures, persistence
- **Memcached**: Simple, high-throughput, no persistence
- **CDN**: Edge caching for static assets (Cloudflare, CloudFront)

## Notes

> Add your personal notes here.
