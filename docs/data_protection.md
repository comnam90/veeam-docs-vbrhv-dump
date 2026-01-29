---
title: "Performing Backup"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/data_protection.html"
last_updated: "8/2/2024"
product_version: "13.7.0.473"
---

# Performing Backup


To produce backups of oVirt VMs, Veeam Plug-in for OLVM and RHV runs backup jobs. A backup job is a collection of settings that define the way backup operations are performed: what data to back up, where to store backups, when to start the backup process, and so on.

One backup job can be used to process multiple VMs, but you can back up each VM with one backup job at a time. If a VM is added to more than one backup job, it will be processed only by the backup job that started earlier.

You can instruct the Veeam Plug-in for OLVM and RHV to run jobs automatically according to a specified schedule or start them manually.

In This Section

* [Creating Backup Jobs](backup_job_create.md)
* [Editing Backup Job Settings](editing_jobs.md)
* [Starting and Stopping Backup Jobs](start_job.md)
* [Analyzing Performance Bottlenecks](bottlenecks.md)
* [Cloning Backup Jobs](cloning_jobs.md)
* [Enabling and Disabling Backup Jobs](disable_jobs.md)
* [Deleting Backup Jobs](delete_jobs.md)
* [Creating Active Full Backups](crearting_active_full_backup.md)
* [Creating VeeamZIP Backups](veeamzip_backup_create.md)


