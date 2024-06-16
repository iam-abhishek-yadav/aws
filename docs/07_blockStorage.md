
## Block Storage - Amazon Elastic Block Store (Amazon EBS)
Amazon Elastic Block Store (Amazon EBS) is block-level storage designed for attachment to Amazon EC2 instances. Similar to attaching an external drive to a laptop, EBS volumes provide detachable, distinct, and size-limited storage that can be connected to one EC2 instance at a time.

- **Detachable:** EBS volumes can be detached from one EC2 instance and attached to another within the same Availability Zone, allowing access to stored data.
- **Distinct:** Similar to an external drive, EBS volumes remain separate from EC2 instances, ensuring data persistence in case of accidents or instance failures.
- **Size-limited:** EBS volumes have a maximum size limit, comparable to the fixed limit of an external drive. For instance, a 2 TB external drive allows storing up to 2 TB of content.

AWS introduced the multi-attach feature for Amazon EBS, enabling Provisioned IOPS SSD (io1 or io2) volumes to be attached to multiple EC2 instances simultaneously in the same Availability Zone.

### Scaling Amazon EBS Volumes
Amazon EBS volumes can be scaled in two ways: increasing volume size or attaching multiple volumes. The volume size can be increased up to the maximum limit of 64 tebibytes (TiB) for supported volumes.

#### Use Cases
1. **Operating Systems:** Quick data retrieval and long-term data persistence.
2. **Databases:** Suitable for database storage needs.
3. **Enterprise Applications:** Reliable storage for various enterprise applications.
4. **Big Data Analytics Engines:** Used in scenarios requiring high-performance storage for big data analytics.

### EBS Volume Types
Amazon EBS volumes are categorized into solid-state drives (SSDs) and hard-disk drives (HDDs), each offering two types.

#### SSD Volumes
- **General Purpose (gp3):** Balances price and performance for a wide variety of workloads.
- **Provisioned IOPS (io1/io2):** Designed for I/O-intensive workloads requiring specific performance levels.

#### HDD Volumes
- **Throughput Optimized (st1):** Ideal for large, sequential workloads requiring high throughput.
- **Cold HDD (sc1):** Low-cost option for less frequently accessed workloads with large data sets.

### Amazon EBS Benefits
- **High Availability:** EBS volumes are automatically replicated in their Availability Zone to prevent data loss.
- **Data Persistence:** Storage remains intact even when associated EC2 instances are not running.
- **Data Encryption:** Supports encryption for enhanced security.
- **Flexibility:** Allows on-the-fly changes to volume type, size, and IOPS capacity without stopping instances.
- **Backups:** Provides the ability to create backups of any EBS volume.

### Amazon EBS Snapshots
EBS snapshots are incremental backups stored redundantly in multiple Availability Zones using Amazon S3. Snapshots are managed through the Amazon EBS console, allowing the creation of multiple new volumes from snapshots.

