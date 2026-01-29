---
title: "VM Backup"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/backup_job_how.html"
last_updated: "11/17/2025"
product_version: "13.7.0.473"
---

# VM Backup


To produce backups of VMs, Veeam Backup & Replication runs backup jobs. A backup job is a collection of settings that define the way backup operations are performed: what data to back up, where to store backups, when to start the backup process, and so on.

How to Protect VMs

1. Check [system requirements](system_requirements.md) and [account permissions](permissions.md).
2. [Add backup repositories](configure_repository.md).
3. [Connect the oVirt KVM Manager](connecting_manager.md).
4. [Configure worker settings](workers_add.md).
5. [Configure notification settings](general_settings.md).
6. [Complete the New Backup Job wizard](backup_job_create.md).

How VM Backup Works

Veeam Plug-in for OLVM and RHV performs VM backup in the following way:

1. Connects to the oVirt KVM Manager over REST API and creates a snapshot of the processed VM.
2. Launches a worker in the same cluster where the processed VM resides.

If no worker is deployed in the cluster, Veeam Backup & Replication launches a worker that is deployed in any other cluster connected to the oVirt KVM Manager. If the backup infrastructure contains another oVirt KVM Manager with deployed workers, Veeam Backup & Replication uses these workers instead.

1. Uses the worker to read VM data from the snapshot created at step 1, transfers the data to the target backup repository and stores it in the native Veeam format.

To reduce the amount of data read from snapshots, Veeam Backup & Replication uses the changed block tracking (CBT) mechanism: during incremental backup sessions, Veeam Backup & Replication sends a REST API request to the oVirt KVM Manager to retrieve only those data blocks that have changed since the previous backup session. If CBT cannot be used, Veeam Backup & Replication reads all data from the snapshots. For more information, see [Changed Block Tracking](changed_block_tracking.md).

Veeam Backup & Replication compresses and deduplicates data saved to repositories.

1. Removes the created snapshot, checks if any other tasks are in the queue and if there are no more sessions queued, suspends the worker when the current backup session completes.

Related Topics

* [Solution Architecture](infrastructure_components.md)
* [Backup Chain](backup.md)
* [VM Restore](restore_how.md)
* [Retention Policies](retention_policies.md)


