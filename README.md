# Game Backend Microservices in Golang

Event-driven microservices backend simulating core game features (player management, inventory, events). Built to explore scalable cloud patterns for game servers.

## Architecture
- Player Service: REST + gRPC, PostgreSQL CRUD, basic auth
- Inventory Service: Calls Player via gRPC, Redis cache for reads
- Event Service: Consumes RabbitMQ messages (e.g., item changes)

## Tech Stack
- Go 1.23+
- gRPC + Protobuf
- Gin (REST)
- RabbitMQ (broker)
- Redis (caching)
- PostgreSQL
- Docker + docker-compose

## Setup
docker-compose up -d

## Goals
- Demonstrate async concurrency (goroutines)
- Eventual consistency via messages
- Horizontal scaling readiness
- Production-like practices (health checks, logging)

In progress — adding tests, metrics, diagram soon.
