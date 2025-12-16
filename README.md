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

