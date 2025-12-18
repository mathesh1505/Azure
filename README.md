# Azure

# 1. Core Azure Architectural Components

Azure architecture is built to provide **high availability, scalability, security, and global reach**.

---

## 1.1 Regions, Availability Zones, Resource Groups

### 🔹 Regions

* A **region** is a geographical area containing one or more data centers.
* Examples: *East US, West Europe, Central India*

**Why Regions matter:**

* Data residency
* Disaster recovery
* Compliance

---

### 🔹 Availability Zones (AZ)

* Physically separate data centers within a region
* Each zone has independent power, cooling, and networking

**Benefits:**

* High availability
* Fault tolerance

Example:

* Deploy VMs across **Zone 1, Zone 2, Zone 3**

---

### 🔹 Resource Groups

* A **logical container** for Azure resources
* Resources share lifecycle (create, update, delete together)

Example:

```
Resource Group: prod-rg
 ├── VM
 ├── Storage Account
 ├── Virtual Network
```

---

## 1.2 Azure Resource Manager (ARM)

ARM is the **deployment and management layer** for Azure.

### Features:

* Infrastructure as Code (IaC)
* Consistent management via:

  * Azure Portal
  * Azure CLI
  * PowerShell
  * ARM templates (JSON/Bicep)

Example ARM concepts:

* Declarative templates
* Role-Based Access Control (RBAC)
* Tags for cost management

---

## 1.3 Azure Compute Options

Azure provides multiple compute choices based on workload needs.

| Service          | Use Case                |
| ---------------- | ----------------------- |
| Virtual Machines | Full OS control         |
| App Services     | Web & API hosting       |
| Containers       | Lightweight apps        |
| Functions        | Event-driven serverless |

---

# 2. Cloud Concepts

---

## 2.1 IaaS, PaaS, SaaS

### 2.1.1 IaaS (Infrastructure as a Service)

You manage:

* OS
* Runtime
* Applications

Azure examples:

* Virtual Machines
* Virtual Networks
* Load Balancers

---

### 2.1.2 PaaS (Platform as a Service)

Azure manages:

* OS
* Runtime
* Scaling

You manage:

* Application code
* Data

Azure examples:

* Azure App Service
* Azure SQL Database

---

### 2.1.3 SaaS (Software as a Service)

Azure manages **everything**.

Examples:

* Microsoft 365
* Dynamics 365
* Power BI

---

## 2.2 Public, Private, Hybrid Cloud Models

### 🔹 Public Cloud

* Resources shared across tenants
* Example: Azure public cloud

### 🔹 Private Cloud

* Dedicated infrastructure
* Example: Azure Stack

### 🔹 Hybrid Cloud

* Combination of on-prem + cloud
* Example: On-prem data center + Azure

---

## 2.3 CapEx vs OpEx

| CapEx             | OpEx           |
| ----------------- | -------------- |
| High upfront cost | Pay-as-you-go  |
| Buy hardware      | Rent resources |
| On-prem           | Cloud          |

Azure follows **OpEx model**.

---

# 3. Azure Compute Services

---

## 3.1 Virtual Machines (VMs)

VMs provide **full control** over OS and applications.

### Use Cases:

* Legacy applications
* Custom software
* Lift-and-shift migrations

---

### 3.1.1 VM Sizing, Pricing & Scaling

#### VM Sizes

* General purpose
* Compute optimized
* Memory optimized
* GPU

#### Pricing

* Pay-as-you-go
* Reserved Instances
* Spot VMs (low cost)

#### Scaling

* Manual scaling
* VM Scale Sets (automatic scaling)

---

### 3.1.2 VM Deployment & Management

Deployment options:

* Azure Portal
* Azure CLI
* ARM/Bicep templates

Management:

* Start/Stop
* Backup
* Monitoring (Azure Monitor)

---

## 3.2 Azure App Services

Fully managed PaaS for hosting:

* Web Apps
* REST APIs
* Mobile backends

### Benefits:

* Auto scaling
* Built-in security
* CI/CD integration
* No server management

---

## 3.3 Azure Functions

Azure Functions is a **serverless compute service**.

### Key Features:

* Event-driven
* Auto scaling
* Pay only for execution time

### Use Cases:

* Data processing
* API backends
* Event triggers

---

## 3.4 Azure Kubernetes Service (AKS)

AKS is a managed Kubernetes service.

### Features:

* Container orchestration
* Auto scaling
* High availability
* Integrated monitoring

### Use Cases:

* Microservices
* Cloud-native applications

---

## 3.5 Cloud Service Models (Summary)

| Model | Control Level | Example       |
| ----- | ------------- | ------------- |
| IaaS  | High          | Azure VMs     |
| PaaS  | Medium        | App Services  |
| SaaS  | Low           | Microsoft 365 |

---

## Why Azure Compute Services Matter

* Flexible workloads
* Cost optimization
* High availability
* Enterprise-grade security

---

# 4. Azure Storage Services

Azure Storage provides scalable, durable, and secure cloud storage solutions.

---

## 4.1 Azure Blob Storage

Azure Blob Storage is an **object storage service** for unstructured data.

### What can be stored?

* Images
* Videos
* Documents
* Backups
* Logs
* Big data files

### Blob Types

* **Block Blob** – Text and binary data (most common)
* **Append Blob** – Logging data
* **Page Blob** – Virtual hard disks (VHD)

### Example Use Cases

* Data lake storage
* Media storage
* Backup & archive

---

## 4.2 Storage Tiers and Replication

### 🔹 Storage Tiers

| Tier    | Use Case                   |
| ------- | -------------------------- |
| Hot     | Frequently accessed data   |
| Cool    | Infrequently accessed data |
| Archive | Long-term backup           |

### 🔹 Replication Options

| Replication | Description               |
| ----------- | ------------------------- |
| LRS         | Locally Redundant Storage |
| ZRS         | Zone Redundant Storage    |
| GRS         | Geo Redundant Storage     |
| GZRS        | Zone + Geo redundancy     |

---

## 4.3 Access Control & Shared Access Signatures (SAS)

### 🔹 Access Control

Azure Storage supports:

* Azure AD (RBAC)
* Storage account keys

### 🔹 SAS (Shared Access Signature)

SAS provides **time-limited and permission-based access**.

Types of SAS:

* Service SAS
* Account SAS
* User Delegation SAS

### Example Use Case

* Grant temporary access to upload/download blobs

---

# 5. Azure Key Vault, Azure Functions & Azure Logic Apps

---

## Azure Key Vault

Azure Key Vault securely stores:

* Secrets (passwords, tokens)
* Keys
* Certificates

### Benefits

* Centralized secret management
* Hardware Security Module (HSM)
* Integration with Azure services

---

## Azure Functions

Azure Functions is a **serverless compute service**.

### Key Features

* Event-driven execution
* Auto scaling
* Pay-per-execution

### Use Cases

* Data processing
* API endpoints
* Event handling

---

## Azure Logic Apps

Logic Apps enables **workflow automation** with low-code/no-code approach.

### Features

* Visual designer
* 400+ connectors
* Built-in error handling

### Use Cases

* Data integration
* Business workflows
* System orchestration

---

# 6. Azure Data Services

---

## 6.1 Azure Data Factory (ADF)

Azure Data Factory is a **cloud ETL/ELT service** for data integration.

---

### 6.1.1 Data Ingestion & Transformation

#### Data Ingestion

* From on-prem, cloud, SaaS
* Supports batch and incremental loads

Sources:

* Azure Blob
* Azure SQL
* AWS S3
* REST APIs

#### Data Transformation

* Mapping Data Flows (no-code)
* Azure Databricks
* Stored procedures

---

### 6.1.2 Pipelines & Activities

#### Pipelines

* Logical grouping of activities

#### Activities

* Copy Activity
* Data Flow Activity
* Lookup Activity
* Web Activity

### Example Pipeline Flow

```
Source → Copy Activity → Data Flow → Sink
```

---

## 6.2 Azure SQL Database

Azure SQL Database is a **fully managed relational database** service.

### Features

* Built-in high availability
* Automatic backups
* Security & encryption

### Service Models

* Single Database
* Elastic Pool
* Managed Instance

### Use Cases

* OLTP workloads
* Cloud-native applications

---

## Why These Azure Services Matter

* Secure data storage
* Scalable data pipelines
* Serverless integration
* Enterprise-grade security

---


