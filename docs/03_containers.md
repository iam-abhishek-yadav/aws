## Containers

Containers are a standardized unit packaging code and dependencies, creating a self-contained environment for reliable execution on any platform.

### Benefits

- **Portability:** Containers facilitate workload movement between environments (e.g., development to production, on-premises to the cloud).
- **Example Platform**
  - **Docker:** A popular container runtime simplifying the management of the entire operating system stack, including networking and storage. Docker aids in creating, packaging, deploying, and running containers.

### Managing Containers with Amazon ECS

#### Overview

- **Service:** Amazon Elastic Container Service (Amazon ECS)
- **Functionality:** End-to-end container orchestration service for container deployment.

#### Deployment Options

- **Serverless Infrastructure:** Managed by AWS Fargate.
- **Controlled Infrastructure:** Run on a cluster of EC2 instances managed by the user.

#### Container Definition

- **Task Definition:** Describes containers, resources (CPU, memory), ports, images, storage, and networking.
- **Format:** JSON file acting as a blueprint.

#### ECS Container Agent

- **Purpose:** Manages communication between container instances and Amazon ECS service.
- **Installation:** Required on EC2 instances, turning them into "container instances."

#### Task Definition Example

```json
{
	"family": "webserver",
	"containerDefinitions": [
		{
			"name": "web",
			"image": "nginx",
			"memory": "100",
			"cpu": "99"
		}
	],
	"requiresCompatibilities": ["FARGATE"],
	"networkMode": "awsvpc",
	"memory": "512",
	"cpu": "256"
}
```

### Kubernetes with Amazon EKS

#### Overview

- **Service:** Amazon Elastic Kubernetes Service (Amazon EKS)
- **Purpose:** Orchestrate containerized workloads and services using Kubernetes in the AWS Cloud.
- **Managed Service:** No need to install, operate, or maintain the Kubernetes control plane or nodes.

#### Kubernetes Overview

- **Definition:** Portable, extensible, open-source platform for managing containerized workloads.
- **Ecosystem:** Popular and well-established, fostering collaboration between development and operations.

#### Amazon ECS vs. Amazon EKS

- **Container Instance Equivalent:**
  - Amazon ECS: EC2 instance with ECS agent.
  - Amazon EKS: Worker node or Kubernetes node.
- **Container Terminology:**
  - Amazon ECS: Task.
  - Amazon EKS: Pod.
- **Underlying Technology:**
  - Amazon ECS: AWS native.
  - Amazon EKS: Kubernetes.

#### Advantages of Amazon EKS

- **Simplicity:** Managed service eliminates manual control plane and node management.
- **High Availability:** Ensures reliability and availability of orchestrated workloads.
- **Fine-Grained Control:** Provides advanced orchestration solutions for greater control over infrastructure.
