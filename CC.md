# Cloud Computing Viva Preparation Notes

# UNIT 1: INTRODUCTION TO CLOUD COMPUTING

## What is Cloud Computing?
Cloud computing is the delivery of computing services such as servers, storage, databases, networking, and software over the internet on a pay-as-you-go basis.

### Examples
- Google Drive
- Gmail
- Netflix
- AWS
- Azure

## Characteristics of Cloud Computing
1. On-Demand Self-Service
2. Broad Network Access
3. Resource Pooling
4. Rapid Elasticity
5. Measured Service

## Benefits
- Cost Saving
- Scalability
- Accessibility
- Backup & Recovery
- High Availability
- Maintenance-Free

## Limitations
- Internet Dependency
- Security Risks
- Downtime
- Vendor Lock-In
- Limited Control

## History of Cloud Computing
- Mainframe Computing
- Cluster Computing
- Grid Computing
- Distributed Computing
- Virtualization

## Virtualization
Creating virtual versions of computing resources such as servers, operating systems, storage, and networks.

### Advantages
- Better Resource Utilization
- Cost Reduction
- Isolation
- Easy Management

## Service-Oriented Computing
Applications/services provided over network.

## Utility-Oriented Computing
Pay only for usage.

## Cloud Platforms
### AWS
- EC2
- S3
- Lambda

### Azure
Enterprise-focused cloud platform.

### GCP
Focused on AI and Big Data.

---

# UNIT 2: PARALLEL & DISTRIBUTED COMPUTING

## Parallel Computing
Multiple processors execute multiple tasks simultaneously.

### Types
- Bit-Level Parallelism
- Instruction-Level Parallelism
- Data Parallelism
- Task Parallelism

## Distributed Computing
Multiple independent computers communicate and work together over a network.

## Parallel vs Distributed Computing

| Parallel Computing | Distributed Computing |
|---|---|
| Multiple processors | Multiple computers |
| Same machine usually | Different systems |
| Focus on speed | Focus on scalability |

## Architectural Styles

### Client-Server
Client sends request, server responds.

### Peer-to-Peer
All systems act equally.

### Multi-Tier Architecture
Presentation, logic, and database layers.

## Challenges in Distributed Systems
- Network Failure
- Synchronization
- Security Risks
- Data Consistency

---

# UNIT 3: VIRTUALIZATION & CLOUD TECHNOLOGY

## Virtualization
Process of creating virtual versions of resources.

## Types of Virtualization

### Full Virtualization
Guest OS unaware of virtualization.

### Para-Virtualization
Guest OS aware of virtualization.

### Hardware Virtualization
Uses hardware support from CPU.

## Hypervisor
Software that creates and manages virtual machines.

### Type 1 Hypervisor
Runs directly on hardware.
Examples:
- VMware ESXi
- Hyper-V

### Type 2 Hypervisor
Runs on operating system.
Examples:
- VirtualBox
- VMware Workstation

## Advantages of Virtualization
- Better Hardware Utilization
- Cost Reduction
- Isolation
- Scalability

## Disadvantages
- Performance Overhead
- Security Risks
- Complex Management

## Data Centers
Facilities containing servers, storage, networking, and cooling systems.

## Containerization
Packaging application and dependencies into lightweight containers.

### Docker
Popular containerization platform.

## VM vs Container

| Virtual Machine | Container |
|---|---|
| Includes full OS | Shares host OS |
| Heavyweight | Lightweight |
| Slower | Faster |

---

# UNIT 4: CLOUD ARCHITECTURE & SERVICE MODELS

## Cloud Architecture
Structure of cloud computing components and services.

### Components
- Frontend
- Backend
- Network
- Storage

## Service Models

### IaaS
Infrastructure as a Service.
Provides VMs, storage, networking.

Examples:
- AWS EC2
- Azure VM

### PaaS
Platform as a Service.
Provides development platform.

Examples:
- Heroku
- Google App Engine

### SaaS
Software as a Service.
Provides ready-to-use software.

Examples:
- Gmail
- Google Docs

## Comparison

| IaaS | PaaS | SaaS |
|---|---|---|
| Infrastructure | Platform | Software |

## Deployment Models

### Public Cloud
Shared cloud over internet.

### Private Cloud
Dedicated cloud for one organization.

### Hybrid Cloud
Combination of public and private cloud.

## Scalability

### Vertical Scaling
Increase power of existing machine.

### Horizontal Scaling
Add more machines.

## Load Balancing
Distributing workload among multiple servers.

## Multi-Tenancy
Multiple users sharing same cloud resources securely.

---

# UNIT 5: DATA-INTENSIVE COMPUTING & MAPREDUCE

## Data-Intensive Computing
Systems designed to process huge amounts of data efficiently.

## Big Data
Large and complex datasets.

### 5 Vs
- Volume
- Velocity
- Variety
- Veracity
- Value

## Hadoop
Open-source framework for distributed storage and processing.

### Components
- HDFS
- MapReduce
- YARN
- Hadoop Common

## HDFS Architecture

### NameNode
Stores metadata and block information.

### DataNode
Stores actual data blocks.

## MapReduce
Distributed programming model for processing large datasets.

### Map Phase
Processes input and generates key-value pairs.

### Reduce Phase
Combines and aggregates results.

## Advantages
- Parallel Processing
- Scalability
- Fault Tolerance

## Limitations
- Slow for real-time processing
- High disk I/O

---

# UNIT 6: CLOUD MANAGEMENT

## Cloud Management
Monitoring and managing cloud resources and services.

## Total Cost of Ownership (TCO)
Complete cost of owning and operating infrastructure.

## CAPEX vs OPEX

| CAPEX | OPEX |
|---|---|
| Upfront investment | Operational expense |
| Buy infrastructure | Rent services |

## Cloud Economics
Financial benefits of cloud computing.

## Resource Management
- Resource Provisioning
- Resource Scheduling
- Resource Monitoring

## SLA (Service Level Agreement)
Contract between provider and customer defining service quality.

### Includes
- Uptime
- Availability
- Performance
- Support

## Cloud Monitoring
Tracking health and performance of cloud services.

## Load Balancing
Distributing workload across servers.

## Autoscaling
Automatically increasing/decreasing resources.

## Challenges
- Security
- Cost Control
- Vendor Lock-In

---

# UNIT 7: CLOUD SECURITY

## Cloud Security
Protection of cloud systems, applications, and data.

## CIA Triad

### Confidentiality
Only authorized users access data.

### Integrity
Data should not be altered improperly.

### Availability
Services should remain accessible.

## Authentication vs Authorization

| Authentication | Authorization |
|---|---|
| Verifies identity | Grants permissions |

## Encryption
Converting readable data into unreadable form.

### Symmetric Encryption
Same key for encryption and decryption.

### Asymmetric Encryption
Uses public and private keys.

## Security Threats
- Data Breach
- Malware
- Insider Threats
- DoS Attacks
- Account Hijacking

## Access Control

### RBAC
Role-Based Access Control.

### ABAC
Attribute-Based Access Control.

## Network Security
- Firewalls
- VPN
- IDS

## Data Security
- Backup & Recovery
- Replication
- Disaster Recovery

## Security Challenges
- Multi-Tenancy Risks
- Compliance Issues
- Data Privacy
- Vendor Dependency
