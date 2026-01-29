---
title: "System Requirements"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/system_requirements.html"
last_updated: "11/17/2025"
product_version: "13.7.0.473"
---

# System Requirements


Before you start deploying Veeam Plug-in for OLVM and RHV, make sure the virtual environment and the backup infrastructure components meet the following requirements.

| Specification | Requirement |
| --- | --- |
| Hypervisor | Kernel-based Virtual Machine (KVM) must be installed on x86 hardware that supports virtualization capabilities. |
| Virtualization Platform | Veeam Plug-in for OLVM and RHV supports the following virtual environments:   * Red Hat Virtualization version 4.4 SP1 only (Red Hat Virtualization Manager version 4.5.0 or later). * Oracle Linux Virtualization Manager version 4.5.4 or later. |
| Veeam Software | Veeam Backup & Replication version 13.0.1.180 with oVirt KVM Plug-in version 13.7.0.473 (or later) must be deployed on the backup server. |
| Workers | VMs running as [workers](workers.md) must be allocated the following compute resources for each concurrent task:   * CPU: 1 vCPU * Memory: 1 GB RAM |

Version Compatibility

The following table lists compatible versions of Veeam Backup & Replication and Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization.

| Product Release | oVirt KVM Plug-in Build | Veeam Backup & Replication Build |
| --- | --- | --- |
| 7 | 13.7.0.473 | 13.0.1.180 |
| 6.2 | 12.6.2.6 | 12.3.2.3617 |
| 6.1 | 12.6.1.4 | 12.3.1.1139 |
| 6.0 | 12.6.0.166 | 12.3.0.310 |
| 5.0 | 12.5.0.299 | 12.2.0.334 |
| 4.1 | 12.4.1.45 | 12.1.2.172 |
| 4.0 | 12.4.0.385 | 12.1.0.2131 |
| 3b | 12.2.3.19 | 12.0.0.1420 |
| 3a | 12.1.3.431 |
| 3.0 | 12.0.3.412 |


