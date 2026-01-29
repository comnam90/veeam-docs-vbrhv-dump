---
title: "Retention Policies"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/retention_policies.html"
last_updated: "11/17/2025"
product_version: "13.7.0.473"
---

# Retention Policies


Backups created by jobs are not kept forever — they are removed according to retention policy settings specified while creating the jobs as described in section [Creating Backup Jobs](backup_job_create.md).

Restore points in the backup chain are stored only for the allowed period of time (in days). If a restore point is older than the specified time limit, Veeam Backup & Replication removes it from the backup chain. To learn how Veeam Backup & Replication applies retention policies to forever forward incremental and forward incremental backup chains, see [Backup Retention](backup_retention.md).

|  |
| --- |
| Note |
| Previous versions of Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization also had a retention policy setting that was based on the number of restore points. For this setting, if the number of allowed restore points was exceeded, Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization removed the earliest restore point from the chain. This functionality is now deprecated. All backup jobs created using the previous version of Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization will be processed according to their existing retention settings, but you will not be able to clone them or create new jobs with retention policy settings based on number of restore points. |


