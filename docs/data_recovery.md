---
title: "Performing Restore"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/data_recovery.html"
last_updated: "8/2/2024"
product_version: "13.7.0.473"
---

# Performing Restore


In various disaster recovery scenarios, Veeam Plug-in for OLVM and RHV allows you to perform the following operations using backed-up data:

* [Entire VM restore](restore_to_rhv.md) — recover oVirt VMs to the original location or to a new location.

* [VM disk restore](restore_disks.md) — recover a specific VM disk and attach it to the original VM or to another VM.
* [Instant VM recovery](instant_vm_recovery.md) — instantly start an oVirt VM directly from a backup.
* [Disk publishing](publish_disk.md) — mount specific disks of a backed-up oVirt VMs to any server added to the backup infrastructure.
* [File-level restore](vm_guest_restore.md) — recover individual VM guest OS files and folders.
* [Application items restore](application_items_restore.md) — restore applications, such as Microsoft Active Directory, Microsoft Exchange, Microsoft SharePoint, and Microsoft SQL Server.
* [VM disk export](vm_disk_export.md) — restore VM disks and convert them to disks of the VMDK, VHD or VHDX format.
* [Performing VM Restore to Amazon Web Services](restore_to_amazon_ec2.md) — restore oVirt VMs to Amazon Web Services as EC2 instances.
* [Performing VM Restore to Microsoft Azure](restore_to_microsoft_azure.md) — restore oVirt VMs to Microsoft Azure as Azure VMs.
* [Performing VM Restore to Google Cloud](restore_to_google_ce.md) — restore oVirt VMs to Google Cloud as VM instances.

You can restore VM data to the most recent state or to any available restore point.


