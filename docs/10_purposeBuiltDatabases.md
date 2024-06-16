## Purpose-built Databases
- Databases designed for specific use cases, addressing the limitations of a one-size-fits-all approach.
- Developers can choose databases based on the needs of their applications.

### AWS Portfolio of Purpose-built Databases

#### Amazon DynamoDB
- Fully managed NoSQL database.
- Provides fast, consistent performance at any scale.
- Flexible billing model and tight integration with Infrastructure as Code (IaC).
- Ideal for high-scale and serverless applications.
- Suitable for online transaction processing (OLTP) workloads.

#### Amazon ElastiCache
- Fully managed in-memory caching solution.
- Supports Redis and Memcached.
- No responsibility for instance failovers, backups, restores, or software upgrades.

#### Amazon MemoryDB for Redis
- Redis-compatible, durable, in-memory database service.
- Ultra-fast performance with microsecond read latency, single-digit millisecond write latency, high throughput, and Multi-AZ durability.
- Can be used as a fully managed, primary database for high-performance applications.

#### Amazon DocumentDB (with MongoDB compatibility)
- Fully managed document database.
- Suitable for content management systems, profile management, web, and mobile applications.
- API compatibility with MongoDB, enabling easy interaction with open-source libraries.

#### Amazon Keyspaces (for Apache Cassandra)
- Scalable, highly available, and managed Apache Cassandra compatible database service.
- Suitable for high-volume applications with straightforward access patterns.
- Allows running Cassandra workloads on AWS using Cassandra Query Language (CQL) code, Apache 2.0 licensed drivers, and tools.

#### Amazon Neptune
- Fully managed graph database.
- Suitable for highly connected data with rich relationships.
- Used for recommendation engines, fraud detection, and knowledge graphs.

#### Amazon Timestream
- Fast, scalable, and serverless time series database service.
- Ideal for Internet of Things (IoT) and operational applications.
- Enables storage and analysis of trillions of events per day with high speed and cost-effectiveness.

#### Amazon Quantum Ledger Database (Amazon QLDB)
- Purpose-built ledger database.
- Provides a complete and cryptographically verifiable history of all changes made to application data.
- Eliminates the need for traditional audit tables and trails.
