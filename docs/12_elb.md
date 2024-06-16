## Load Balancers

Load balancing distributes tasks across a set of resources. These resources are often EC2 instances hosting an application, and the tasks are requests sent to the application. Load balancers use algorithms like round-robin to redirect traffic, ensuring efficient resource utilization and high availability.

### Elastic Load Balancer (ELB)

AWS provides the Elastic Load Balancer (ELB) service for load balancing. ELB sits directly in the path of traffic, efficiently distributing requests across multiple resources.

#### ELB Features

- **Automatic Scaling:** ELB scales automatically to handle incoming traffic demand, ensuring consistent performance.
- **Hybrid Mode Support:** ELB supports hybrid mode, providing seamless integration with on-premises resources.
- **High Availability and Scalability:** ELB ensures high availability and scalability, essential for mission-critical applications.

#### Health Checks

ELB performs health checks to ensure that traffic is routed only to healthy EC2 instances. These health checks involve establishing connections or making HTTP/HTTPS requests to verify the health of resources.

#### ELB Components

The main components of ELB include rules, listeners, and target groups. Rules define how incoming traffic is routed, listeners configure the protocol and port for accepting traffic, and target groups define the set of resources that receive traffic.

### Types of Load Balancers

- **Application Load Balancer (ALB):** Operates at Layer 7 (OSI model) and is ideal for HTTP and HTTPS traffic. It routes traffic based on request content.
- **Network Load Balancer (NLB):** Operates at Layer 4 (OSI model) and is ideal for TCP and UDP traffic. It preserves client-side source IP addresses.
- **Gateway Load Balancer (GLB):** Designed for third-party virtual appliances, aiding in deployment, scaling, and management.

#### ALB Features

- **Content-Based Routing:** ALB routes traffic based on request data, offering granular control over traffic distribution.
- **TLS Offloading:** ALB supports TLS offloading, authenticating users and securing traffic.
- **Layer 7 Load Balancing:** ALB operates at the application layer (Layer 7) of the OSI model, making it ideal for routing based on content, such as HTTP/HTTPS.
- **Path-Based and Host-Based Routing:** ALB supports path-based and host-based routing, enabling efficient traffic distribution for various backend services.
- **WebSocket Support:** ALB natively supports WebSocket communication, making it suitable for real-time applications.
- **Integration with AWS Services:** ALB seamlessly integrates with other AWS services like AWS WAF for enhanced security.

#### NLB Features

- **Static IP Support:** NLB provides static IP addresses, ensuring consistent addressing for applications.
- **Low Latency:** NLB is designed for low-latency performance, making it suitable for latency-sensitive applications.
- **Layer 4 Load Balancing:** NLB operates at the transport layer (Layer 4) of the OSI model, making it suitable for TCP, UDP, and TLS traffic.
- **Static IP Addresses:** NLB provides static IP addresses, ensuring consistent and predictable addressing for applications.
- **High Throughput and Low Latency:** NLB is designed for high throughput and low-latency performance, making it suitable for latency-sensitive applications.
- **Cross-Zone Load Balancing:** NLB offers cross-zone load balancing, distributing traffic evenly across instances in all availability zones.

#### GLB Features

- **High Availability:** GLB offers high availability, monitoring, and streamlined deployments.
- **Scalability:** GLB scales horizontally to handle increased load, providing elasticity for changing traffic patterns.
- **Virtual Appliance Support:** GLB supports third-party virtual appliances, simplifying deployment and management.
- **Fully Managed:** GWLB is a fully managed service that simplifies the deployment and management of high-performance, scalable load balancing.
- **Support for Virtual Appliances:** GWLB supports the deployment of third-party virtual appliances, allowing for advanced networking and security functionalities.
- **IPv4 and IPv6 Dual Stack:** GWLB is IPv4 and IPv6 dual-stack capable, providing flexibility for modern network architectures.
- **Scalability and Elasticity:** GWLB scales horizontally to handle increased load and provides elasticity to adapt to changing traffic patterns.

### Use Cases

- **ALB Use Cases:** Web applications with multiple backend services, microservices architecture requiring path-based or host-based routing, real-time applications using WebSocket communication.
- **NLB Use Cases:** TCP/UDP-based applications with high throughput and low latency requirements, applications requiring a static IP address for consistent addressing.
- **GWLB Use Cases:** Scalable and fully managed load balancing for virtual appliances, IPv6-enabled architectures requiring dual-stack support.

### Best Practices

- **ALB Best Practices:** Leverage path-based and host-based routing for efficient traffic distribution, utilize ALB access logs for monitoring and analysis, enable AWS WAF for additional security measures.
- **NLB Best Practices:** Optimize NLB for high-throughput applications with appropriate target types, use static IP addresses for consistency in addressing, leverage NLB's built-in support for fault tolerance.
- **GWLB Best Practices:** Deploy GWLB across multiple availability zones for high availability, utilize GWLB for scalability and adaptability to varying workloads, leverage dual-stack capabilities for IPv4 and IPv6 support.

#### Selecting Between ELB Types

| Feature                    | ALB                  | NLB               | GLB                                        |
| -------------------------- | -------------------- | ----------------- | ------------------------------------------ |
| Load Balancer Type         | Layer 7              | Layer 4           | Layer 3 gateway and Layer 4 load balancing |
| Target Type                | IP, instance, Lambda | IP, instance, ALB | IP, instance                               |
| Protocol Listeners         | HTTP, HTTPS          | TCP, UDP, TLS     | IP                                         |
| Static IP and Elastic IP   |                      | Yes               |                                            |
| Preserve Source IP Address | Yes                  | Yes               | Yes                                        |
| Fixed Response             | Yes                  |                   |                                            |
| User Authentication        | Yes                  |                   |                                            |
