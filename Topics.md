### Infrastructure & Core Systems

🔥 **Very Common** — Design a URL Shortener (TinyURL)

* Hashing, redirects, analytics, expiry
* Almost universal at every company

🔥 **Very Common** — Design a Rate Limiter

* Token bucket vs sliding window
* Distributed vs single-node
* Redis patterns

🔥 **Very Common** — Design a Distributed Cache (Redis-like)

* Eviction policies
* Consistency
* Cluster sharding
* TTL

🔥 **Very Common** — Design an API Gateway / Reverse Proxy

* Auth
* Rate limiting
* Load balancing
* Routing
* Observability

🟡 **Common** — Design a Distributed Job Scheduler / Task Queue

* Cron-like scheduling
* Retries
* Backpressure
* Exactly-once semantics

🟡 **Common** — Design a Key-Value Store (DynamoDB-like)

* LSM trees
* Consistent hashing
* Quorum reads/writes
* Conflict resolution

---

### Social / Feed Systems

🔥 **Very Common** — Design a News Feed / Social Timeline (Facebook / Twitter)

* Fan-out on write vs read
* Ranking
* Pagination
* Cache warming

🔥 **Very Common** — Design Instagram / Photo Sharing

* Object storage
* CDN
* Metadata DB
* Feed generation
* Follow graph

🔥 **Very Common** — Design a Notification System

* Push vs pull
* Fan-out
* Deduplication
* Delivery guarantees
* Channels (email/SMS/push)

🟡 **Common** — Design Twitter Search / Type-Ahead

* Inverted index
* Trie
* Trending topics
* Eventual consistency

🟡 **Common** — Design a Recommendation Engine

* Collaborative filtering
* Embedding lookups
* Feature stores
* A/B testing

---

### Storage & Data Systems

🔥 **Very Common** — Design Google Drive / Dropbox (File Storage)

* Chunking
* Deduplication
* Versioning
* Sync
* Metadata service

🔥 **Very Common** — Design a Distributed Message Queue (Kafka-like)

* Partitions
* Consumer groups
* Offsets
* Replication
* Exactly-once

🟡 **Common** — Design a Distributed File System (HDFS-like)

* NameNode vs DataNode
* Replication factor
* Block-size trade-offs

🟡 **Common** — Design a Web Crawler

* URL frontier
* Politeness
* Deduplication
* Parallel fetchers
* Storage

⚪ **Occasional** — Design a Metrics & Monitoring System (Prometheus-like)

* Time-series DB
* Scraping
* Alerting
* Cardinality management

---

### Real-Time & Communication

🔥 **Very Common** — Design a Chat System (WhatsApp / Slack)

* WebSockets
* Message ordering
* Online presence
* Group messaging
* E2E encryption

🔥 **Very Common** — Design a Live Video Streaming Platform (YouTube Live)

* RTMP ingest
* HLS/DASH
* CDN edge
* Transcoding pipeline
* Latency vs scale

🟡 **Common** — Design a Ride-Sharing System (Uber / Lyft)

* Geo-indexing
* Matching
* Surge pricing
* Real-time location updates

🟡 **Common** — Design a Collaborative Document Editor (Google Docs)

* OT vs CRDTs
* Presence
* Conflict resolution
* Persistence

⚪ **Occasional** — Design a Live Sports Scoreboard

* Push updates at scale
* Fan-out
* Caching hot data
* Eventual consistency

---

### API & Platform Design

🔥 **Very Common** — Design a Search Autocomplete / Type-Ahead Service

* Trie vs inverted index
* Personalization
* Latency budget
* Ranking

🔥 **Very Common** — Design a Payment / Checkout System

* Idempotency
* Distributed transactions
* Fraud detection
* State machine

🟡 **Common** — Design a Hotel / Flight Booking System (Booking.com)

* Inventory
* Concurrent reservations
* 2-phase commit
* Pricing

🟡 **Common** — Design an E-commerce Product Catalogue & Search

* Elasticsearch
* Faceting
* Inventory service
* Reviews
* CDN for images

⚪ **Occasional** — Design an OAuth2 / SSO Service

* Token lifecycle
* Refresh tokens
* Scopes
* PKCE
* Multi-tenant authentication

### Top 10 Most Frequently Asked in FAANG/System Design Interviews

1. URL Shortener (TinyURL)
2. Rate Limiter
3. News Feed (Facebook/Twitter)
4. Distributed Cache (Redis)
5. Chat System (WhatsApp)
6. Instagram / Photo Sharing
7. Notification System
8. Kafka-like Message Queue
9. API Gateway / Reverse Proxy
10. Search Autocomplete / Type-Ahead

Given your backend experience (Node.js, Kafka, MongoDB, scalable systems), mastering these 10 will cover a large portion of SDE-2 level system design interviews.
