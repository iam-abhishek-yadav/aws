## AWS Security with Security Groups and Network Access Control Lists (NACLs)

Amazon Web Services (AWS) incorporates robust security measures within its cloud infrastructure to safeguard resources and data. Two key elements contributing to network security in AWS are Security Groups and Network Access Control Lists (NACLs). Let's delve into their functionalities:

### Security Groups:

- **Definition and Role:**

- Security Groups serve as virtual firewalls for Amazon EC2 instances (virtual servers) at the instance level.

- They regulate both inbound and outbound traffic by allowing or denying specific protocols, ports, and IP addresses.

- **Association and Rules:**

- Each EC2 instance can be linked with one or more security groups, each comprising distinct inbound and outbound rules.

- Inbound rules dictate the permissible incoming traffic, while outbound rules control the traffic leaving the instance.

- **Configuration:**

- Security Groups can be configured using various parameters such as IP addresses, CIDR blocks, security group IDs, or DNS names to specify traffic source or destination.

- Operating at the instance level, they assess rules before permitting traffic to reach the instance.

- **Statefulness:**

- Security Groups operate on a stateful basis, automatically allowing corresponding outbound traffic if an inbound rule permits traffic, and vice versa.

- Changes made to security group rules take immediate effect.

### Network Access Control Lists (NACLs):

- **Additional Security Layer:**

- NACLs function as an additional security layer operating at the subnet level, serving as stateless traffic filters for both inbound and outbound traffic at the subnet boundary.

- **Association and Uniqueness:**

- Unlike Security Groups, NACLs are associated with subnets, where each subnet can have only one NACL, but multiple subnets can share the same NACL.

- **Rule Structure:**

- NACLs are comprised of a sequentially numbered list of rules, evaluated from lowest to highest.

- Each rule includes specific criteria such as rule number, protocol, rule action (allow or deny), source or destination IP address range, port range, and ICMP type.

- **Configuration Flexibility:**

- NACL rules can be configured to allow or deny specific types of traffic based on the defined criteria.

- **Statelessness:**

- NACLs are stateless, requiring explicit allowance for corresponding outbound traffic through a separate outbound rule if an inbound rule permits traffic.

- Changes made to NACL rules may take some time to propagate across all resources using the associated subnet.
