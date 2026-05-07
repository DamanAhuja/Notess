# ☁️ CLOUD COMPUTING — UNIT 1 (FULL VIVA PREP)

# 🔷 UNIT 1: INTRODUCTION TO CLOUD COMPUTING

---

# 1. ☁️ What is Cloud Computing?

### 💡 Definition
Cloud computing is the delivery of computing services such as:
- servers
- storage
- databases
- networking
- software

over the internet on a pay-as-you-go basis.

---

# 🔑 Simple Explanation

Instead of buying expensive hardware:
👉 users rent computing resources online.

---

# 🔥 Real-Life Examples
- Google Drive
- Gmail
- Netflix
- AWS
- Azure

---

# 🔥 Viva Question
👉 “Why is it called cloud computing?”

Because services/resources are accessed over the internet, represented symbolically as a “cloud.”

---

# 2. 🧠 Characteristics of Cloud Computing

VERY IMPORTANT.

---

## 🔹 1. On-Demand Self-Service
Users can get resources anytime automatically.

Example:
Creating a VM on AWS instantly.

---

## 🔹 2. Broad Network Access
Accessible through internet from anywhere.

---

## 🔹 3. Resource Pooling
Resources shared among multiple users.

---

## 🔹 4. Rapid Elasticity
Resources can scale up/down quickly.

---

## 🔹 5. Measured Service
Pay only for what you use.

---

# 🔥 Viva
👉 “What is elasticity?”

Ability to dynamically scale resources according to demand.

---

# 3. ✅ Benefits of Cloud Computing

---

## 🔹 Cost Saving
No need to buy infrastructure.

---

## 🔹 Scalability
Easy expansion of resources.

---

## 🔹 Accessibility
Access from anywhere.

---

## 🔹 Backup & Recovery
Cloud providers maintain backups.

---

## 🔹 High Availability
Services available most of the time.

---

## 🔹 Maintenance-Free
Provider handles updates.

---

# 🔥 Viva
👉 “Why do companies move to cloud?”

Lower cost, scalability, flexibility, and easier maintenance.

---

# 4. ❌ Limitations / Challenges

---

## 🔹 Internet Dependency
Requires internet connection.

---

## 🔹 Security Risks
Data stored online.

---

## 🔹 Downtime
Cloud provider failures affect users.

---

## 🔹 Vendor Lock-In
Hard to switch providers.

---

## 🔹 Limited Control
Infrastructure controlled by provider.

---

# 🔥 Viva
👉 “Biggest disadvantage of cloud?”

Security and dependency on internet/provider.

---

# 5. 📜 HISTORY OF CLOUD COMPUTING

VERY IMPORTANT.

---

# 🔹 Mainframe Computing

### 💡 Idea:
One large central computer serves many users.

---

### Characteristics:
- Expensive
- Centralized
- Shared terminals

---

# 🔹 Cluster Computing

### 💡 Definition:
Multiple computers connected together acting as one system.

---

### Purpose:
Increase performance & reliability.

---

### Example:
Supercomputers.

---

# 🔥 Viva
👉 “Cluster computing vs distributed computing?”

Cluster:
- tightly connected
- same location

Distributed:
- loosely connected
- different locations

---

# 🔹 Grid Computing

### 💡 Definition:
Computers from different locations work together on tasks.

---

### Example:
Scientific computations.

---

### Difference from Cluster:
Grid systems are geographically distributed.

---

# 🔹 Distributed Computing

### 💡 Definition:
Tasks distributed among multiple independent systems.

---

### Example:
Google Search servers.

---

# 🔹 Virtualization (MOST IMPORTANT)

This is the core technology behind cloud.

---

# 6. 🧠 What is Virtualization?

### 💡 Definition
Virtualization is the creation of virtual versions of computing resources such as:
- servers
- operating systems
- storage
- networks

---

# 🔥 Simple Meaning

One physical computer can run multiple virtual machines.

---

# 🔥 Example

One server running:
- Windows VM
- Linux VM
- Ubuntu VM

simultaneously.

---

# 🔥 Why Important?

Without virtualization:
- cloud scalability becomes difficult
- hardware utilization becomes poor

---

# 🔥 Advantages

## 🔹 Better Resource Utilization
## 🔹 Cost Reduction
## 🔹 Isolation
One VM crash doesn’t affect others.

## 🔹 Easy Management

---

# 🔥 Viva
👉 “What enables cloud computing?”

Virtualization.

---

# 7. 🏗️ Service-Oriented Computing

### 💡 Definition
Applications/services provided over network.

---

### Examples
- Gmail
- Office 365
- Google Docs

---

# 🔥 Key Idea
Users consume services without worrying about infrastructure.

---

# 8. ⚡ Utility-Oriented Computing

### 💡 Definition
Computing resources provided like utilities:
- electricity
- water

Pay only for usage.

---

# 🔥 Example
AWS billing.

---

# 🔥 Viva
👉 “What is pay-as-you-go model?”

Users are charged only for consumed resources.

---

# 9. ☁️ CLOUD PLATFORMS

# 🔹 AWS (Amazon Web Services)

Largest cloud provider.

## Important Services
### EC2
Virtual machines.

### S3
Cloud storage.

### Lambda
Serverless computing.

---

# 🔥 Viva
👉 “Why is AWS popular?”

Scalable, reliable, huge service ecosystem.

---

# 🔹 Microsoft Azure

Popular among enterprises.

### Services
- Virtual Machines
- Azure SQL
- AI services

---

# 🔹 Google Cloud Platform (GCP)

Strong in:
- AI
- Big data
- analytics

### Services
- Compute Engine
- Firebase
- BigQuery

---

# 🔥 MOST IMPORTANT VIVA QUESTIONS (UNIT 1)

## 1. What is cloud computing?
## 2. Characteristics of cloud computing?
## 3. Benefits & limitations?
## 4. Explain virtualization.
## 5. Difference between cluster and grid computing?
## 6. What is utility computing?
## 7. Explain pay-as-you-go.
## 8. AWS vs Azure vs GCP?
## 9. What enabled modern cloud computing?
👉 Virtualization

---

# ⚡ QUICK REVISION

- Cloud = services over internet
- Pay-as-you-go model
- Elasticity = scaling resources
- Virtualization = multiple VMs on one system
- Cluster = tightly connected systems
- Grid = geographically distributed
- AWS = biggest provider
- GCP = AI-focused
- Azure = enterprise-focused

---

# ☁️ CLOUD COMPUTING — UNIT 2 (FULL VIVA PREP)

# 🔷 PARALLEL & DISTRIBUTED COMPUTING

# 1. 🧠 What is Parallel Computing?

### 💡 Definition
Parallel computing is a type of computation where multiple processors execute multiple tasks simultaneously to solve a problem faster.

# 2. 🌐 What is Distributed Computing?

### 💡 Definition
Distributed computing is a system where multiple independent computers communicate and work together over a network.

# 🔥 PARALLEL vs DISTRIBUTED COMPUTING

| Parallel Computing | Distributed Computing |
|---|---|
| Multiple processors | Multiple computers |
| Usually same machine | Different systems |
| Shared memory common | Message passing common |
| High-speed execution | Resource sharing |
| Tightly coupled | Loosely coupled |

# 🔷 Architectural Styles

## Client-Server Architecture
Client sends request → server responds.

## Peer-to-Peer Architecture
All systems act equally as both client and server.

## Multi-Tier Architecture
Presentation layer, business layer, database layer.

---

# ☁️ CLOUD COMPUTING — UNIT 3 (FULL VIVA PREP)

# 🔷 VIRTUALIZATION & CLOUD TECHNOLOGY

# 🧠 What is Virtualization?

### 💡 Definition
Virtualization is the process of creating virtual versions of computing resources.

# 🔷 TYPES OF VIRTUALIZATION

## Full Virtualization
Guest OS unaware of virtualization.

## Para-Virtualization
Guest OS aware of virtualization.

## Hardware Virtualization
Uses hardware support from CPU.

# 🧠 HYPERVISOR

### 💡 Definition
Software that creates and manages virtual machines.

## Type 1 Hypervisor
Runs directly on hardware.

Examples:
- VMware ESXi
- Hyper-V

## Type 2 Hypervisor
Runs on operating system.

Examples:
- VirtualBox
- VMware Workstation

# 📦 CONTAINERIZATION

### 💡 Definition
Packaging application + dependencies together into lightweight containers.

# 🐳 DOCKER
Docker is a containerization platform.

# ⚔️ VM vs CONTAINER

| Virtual Machine | Container |
|---|---|
| Includes full OS | Shares host OS |
| Heavyweight | Lightweight |
| Slower startup | Faster startup |

---

# ☁️ CLOUD COMPUTING — UNIT 4 (FULL VIVA PREP)

# 🔷 CLOUD COMPUTING ARCHITECTURE & SERVICE MODELS

# 🧠 What is Cloud Architecture?

### 💡 Definition
Cloud architecture is the structure of cloud computing components and services working together.

# 🔷 COMPONENTS OF CLOUD ARCHITECTURE

- Frontend
- Backend
- Network
- Storage

# ☁️ SERVICE MODELS

## IaaS
Infrastructure as a Service.

Examples:
- AWS EC2
- Azure VM

## PaaS
Platform as a Service.

Examples:
- Heroku
- Google App Engine

## SaaS
Software as a Service.

Examples:
- Gmail
- Google Docs

# 🔥 COMPARISON

| IaaS | PaaS | SaaS |
|---|---|---|
| Infrastructure | Platform | Software |

# ☁️ DEPLOYMENT MODELS

## Public Cloud
Shared cloud over internet.

## Private Cloud
Dedicated cloud for one organization.

## Hybrid Cloud
Combination of public + private cloud.

# ⚡ LOAD BALANCING

### 💡 Definition
Distributing workload among multiple servers.

---

# ☁️ CLOUD COMPUTING — UNIT 5 (FULL VIVA PREP)

# 🔷 DATA-INTENSIVE COMPUTING & MAPREDUCE PROGRAMMING

# 📊 What is Data-Intensive Computing?

Systems designed to process huge amounts of data efficiently.

# 🧠 What is Big Data?

Large and complex datasets.

# 🔥 5 Vs of Big Data

- Volume
- Velocity
- Variety
- Veracity
- Value

# 🏢 HADOOP

### 💡 Definition
Hadoop is an open-source framework used for distributed storage and distributed processing of big data.

# 🧩 COMPONENTS OF HADOOP

- HDFS
- MapReduce
- YARN
- Hadoop Common

# 🏗️ HDFS ARCHITECTURE

## NameNode
Stores metadata.

## DataNode
Stores actual data blocks.

# 🧠 MAPREDUCE

### 💡 Definition
MapReduce is a distributed programming model used for processing large datasets in parallel.

## MAP PHASE
Processes input data and generates key-value pairs.

## REDUCE PHASE
Combines and aggregates results.

---

# ☁️ CLOUD COMPUTING — UNIT 6 (FULL VIVA PREP)

# 🔷 CLOUD MANAGEMENT

# 🧠 What is Cloud Management?

Monitoring and managing cloud resources and services.

# 💰 TOTAL COST OF OWNERSHIP (TCO)

Complete cost of owning and operating IT infrastructure.

# 💸 CAPEX vs OPEX

| CAPEX | OPEX |
|---|---|
| Upfront investment | Operational expense |
| Buy infrastructure | Rent services |

# 📜 SERVICE LEVEL AGREEMENT (SLA)

Contract between cloud provider and customer defining expected service quality.

# ⚡ LOAD BALANCING

Distributing workloads among multiple servers.

# 🛠️ AUTOSCALING

Automatically increasing/decreasing resources based on workload.

---

# ☁️ CLOUD COMPUTING — UNIT 7 (FULL VIVA PREP)

# 🔷 CLOUD SECURITY

# 🔐 What is Cloud Security?

Protection of cloud systems, applications, and data from threats and attacks.

# 🧠 CIA TRIAD

## Confidentiality
Only authorized users can access data.

## Integrity
Data should not be altered improperly.

## Availability
Services should remain accessible.

# 🔑 AUTHENTICATION vs AUTHORIZATION

| Authentication | Authorization |
|---|---|
| Verifies identity | Grants permissions |

# 🔒 ENCRYPTION

Converting readable data into unreadable form.

## Symmetric Encryption
Same key used for encryption and decryption.

## Asymmetric Encryption
Uses public and private keys.

# ⚠️ CLOUD SECURITY THREATS

- Data Breach
- Malware Attacks
- Insider Threats
- Denial of Service (DoS)
- Account Hijacking

# 🔥 MOST IMPORTANT VIVA QUESTIONS (UNIT 7)

## 1. What is cloud security?
## 2. Explain CIA triad.
## 3. Authentication vs authorization?
## 4. What is encryption?
