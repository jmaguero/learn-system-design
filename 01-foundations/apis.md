# 🔌 APIs

## REST
- Stateless, uses HTTP verbs (GET, POST, PUT, DELETE)
- Resource-based URLs
- Returns JSON/XML

## GraphQL
- Client specifies exactly what data it needs
- Single endpoint (`/graphql`)
- Avoids over-fetching and under-fetching

## gRPC
- Uses Protocol Buffers (binary, compact)
- Supports bidirectional streaming
- Best for internal service-to-service communication

## Comparison

| Feature | REST | GraphQL | gRPC |
|---|---|---|---|
| Protocol | HTTP | HTTP | HTTP/2 |
| Format | JSON | JSON | Protobuf |
| Schema | OpenAPI | SDL | Proto files |
| Streaming | Limited | Subscriptions | Native |
| Best For | Public APIs | Flexible queries | Microservices |

## Notes

> Add your personal notes here.
