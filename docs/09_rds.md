
## Amazon RDS 

- **Amazon RDS:** Managed database service for creating and managing relational databases in the cloud.
- **Operational Burden:** Eliminates the operational burden of traditional database management.
- **Focus:** Allows users to focus on application-specific tasks, reducing infrastructure-related tasks.

### Supported Engines

- **Commercial Options:**
  - Oracle
  - SQL Server
- **Open Source Options:**
  - MySQL
  - PostgreSQL
  - MariaDB
- **Cloud Native:**
  - Aurora

### Database Instances

- **Compute and Storage Components:**
  - **DB Instance:** Composed of compute (DB instance) and storage (Amazon EBS volumes).
- **Engine Variation:** Different engines result in varying supported features and configurations.
- **EC2 Instance Management:** Handled through the Amazon RDS console.

### Storage

- **Storage for DB Instances:**
  - Utilizes Amazon Elastic Block Store (Amazon EBS) volumes.
  - Aurora uses cluster volumes for data storage.
- **Storage Types:**
  - General Purpose SSD (gp2 and gp3)
  - Provisioned IOPS SSD (io1)
  - Magnetic (standard)

### Amazon VPC Integration

- **DB Instance Configuration:**
  - Selection of Amazon Virtual Private Cloud (Amazon VPC) and subnets.
  - DB Subnet Group: Ensures private subnets for enhanced security.
  - Network Access Control Lists (network ACLs) and Security Groups for fine-grained control.

### Backup Strategies

#### Automated Backups

- **Default Setting:** Turned on by default.
- **Backup Window:** Set during a period of low database activity.
- **Retention Period:** Between 0 and 35 days.
- **Point-in-Time Recovery:** Creates a new DB instance using data restored from a specific point in time.

#### Manual Snapshots

- **Longer Retention:** Useful for retaining backups beyond 35 days.
- **Recommended Strategy:** Deploy both automated backups and manual snapshots.

### Multi-AZ Deployment

- **Redundancy:** Creates a redundant copy of the database in another Availability Zone (Multi-AZ).
- **Primary and Standby Copy:** Ensures availability with two synchronized copies.
- **Automatic Failover:** Initiates in case of primary database connectivity loss.
- **DNS Name:** Used for failover to the standby database.

### Security in Amazon RDS

#### IAM (Identity and Access Management)

- **Access Control:**
  - Manages access to Amazon RDS resources.
  - Allows specifying tasks and resources that users can access.
  
#### Security Groups

- **Traffic Control:**
  - Network-level access control.
  - Defines rules for inbound and outbound traffic.
  - Granular control over allowed communication.

#### RDS Encryption

- **Data Protection:**
  - Encrypts data at rest to enhance security.
  - Uses industry-standard encryption algorithms.
  - Applies to storage, automated backups, and snapshots.

#### SSL/TLS (Secure Sockets Layer/Transport Layer Security)

- **Secure Communication:**
  - Ensures secure communication between applications and databases.
  - Uses encryption to protect data during transmission.
  - Mandatory for compliance and data integrity.

