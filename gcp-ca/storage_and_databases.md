# Storage & Databases

## Storage Options

### Cloud Storage

- Consistent, scalable, large-capacity, highly durable `object storage`.
- `11 9’s Durability` (99.999999999%).
- `Unlimited storage` with no minimum object size.
- Use Cloud Storage for `content delivery`, `data lakes`, and `backup`.
- Available in different `storage classes` and `availability`.
- Storage Classes
    - Standard
        - Maximum availability and no limitations.
    - Nearline
        - Low-cost archival storage.
        - Accessed <1/month.
    - Coldline
        - Even lower-cost archival storage.
        - Accessed <1/quarter.
    - Archive
        - Lowest-cost archival storage.
        - Accessed <1/year.
- Availability
    - Region
    - Single Region 
    - Dual-region
    - Pair of regions 
    - Multi-region
    - Large geographic area 

### Filestore

- Fully managed `NFS file server`.
- `NFSv3` compliant.
- `Store data` from running applications.
- Use with VM `instances` and `Kubernetes clusters`.

### Persistent Disks

- `Durable block storage` for instances.
    - `Standard` – Regular standard storage at a reasonable price.
    - `Solid State (SSD)` - Lower latency/higher IOPS.
    - Both options are available in `zonal` and `regional` options

## Database Options

### Cloud SQL

- Fully managed database service.
- PostgreSQL, MySQL, and SQL Server.
- High availability across zones.

### Cloud Spanner

- Scalable relational database service.
- Support transactions, strong consistency and synchronous replication.
- High availability across regions and globally.

### Bigtable

- Fully managed, scalable NoSQL database.
- High throughput with low latency.
- Cluster resizing without downtime. 

### Datastore

- Fast, fully managed, serverless, NoSQL document database.
- For mobile, web and IoT apps.
- Multi-region replication and ACID transactions. 

### Firestore

- NoSQL, realtime database.
- Optimized for offline use.
- Cluster resizing without downtime. 

### Memorystore

- Highly available in-memory service for Redis and Memcached
-Fully Managed 
