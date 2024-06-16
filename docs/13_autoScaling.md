
## Capacity Issues

### Vertical Scaling

#### Increase the instance size
- Vertical scaling is applicable to active-passive systems.
- It involves increasing the size of the server to handle more requests.
- Steps:
  1. Stop the passive instance (not taking traffic).
  2. Change the instance size or type.
  3. Start the instance.
  4. Shift traffic to the passive instance, making it active.
  5. Stop, change size, and start the previous active instance.
- Manual process with limitations on scalability.

### Horizontal Scaling

#### Add more servers
- Applicable to active-active systems.
- Involves scaling horizontally by adding more servers.
- Provides better scalability and avoids limitations of vertical scaling.


## Traditional Scaling vs. Auto Scaling

### Traditional Scaling
- Provision enough servers for peak traffic.
- May result in over-provisioning or under-provisioning during off-peak hours.
- Wasteful use of resources and increased costs.

### Auto Scaling with Amazon EC2

#### Features
1. **Automatic scaling:** Scales in and out based on demand.
2. **Scheduled scaling:** Scales based on user-defined schedules.
3. **Fleet management:** Automatically replaces unhealthy EC2 instances.
4. **Predictive scaling:** Uses machine learning to optimize the number of EC2 instances.
5. **Purchase options:** Multiple models, instance types, and Availability Zones.
6. **Amazon EC2 availability:** Integrated with Amazon EC2 service.


## Amazon EC2 Auto Scaling with ELB

- ELB integrates seamlessly with Amazon EC2 Auto Scaling.
- ELB is notified when a new EC2 instance is added or removed.
- ELB validates the application's availability on the new instance using health checks.


## Amazon EC2 Auto Scaling Components

### Launch Templates and Configurations

- **Launch template:** Stores instance configuration information.
- Supports versioning for easy rollback.
- Specify parameters like AMI ID, instance type, security groups.
- Can be created from an existing EC2 instance, template, or from scratch.

### Amazon EC2 Auto Scaling Groups

- Define where EC2 instances are deployed.
- Specify Amazon VPC, subnets, and type of purchase (On-Demand, Spot, or a mix).
- Configure capacity settings and desired number of instances.
- Ensures instances are created across different Availability Zones.

### Scaling Policies

- Default: Auto Scaling group stays at its initial desired capacity.
- Scaling policies use CloudWatch metrics and alarms.
- Types of scaling policies:
  1. **Simple Scaling Policy:** Adjusts the capacity based on a single, specified metric.
  2. **Step Scaling Policy:** Adds or removes capacity based on specified adjustments.
  3. **Target Tracking Scaling Policy:** Adjusts capacity to maintain a target metric value.
