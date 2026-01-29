---
title: "Copying Backups to Tapes"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/backup_tape_jobs.html"
last_updated: "11/18/2025"
product_version: "13.7.0.473"
---

# Copying Backups to Tapes


You can create archives of oVirt VM backups and copy them to tapes for long-term storage. Veeam Plug-in for OLVM and RHV allows you to manage tape archives the same way you manage backups in backup repositories. However, it usually takes more time to access archived data on tapes than to access backed-up data in repositories. For more information on tapes, see the Veeam Backup & Replication User Guide, section [Tape Devices Support](https://tw-preview.dev.amust.local/html/vbr/13.0.1/userguide/tape_device_support.html?ver=13).

To archive oVirt VM backups to tape, do the following:

1. Configure the tape infrastructure:

1. Connect tape devices as described in the Veeam Backup & Replication User Guide, section [Tape Devices Deployment](https://tw-preview.dev.amust.local/html/vbr/13.0.1/userguide/tape_deployment.html?ver=13).
2. Perform initial configuration of the tape infrastructure as described in the Veeam Backup & Replication User Guide, section [Getting Started with Tapes](https://tw-preview.dev.amust.local/html/vbr/13.0.1/userguide/getting_started_with_tapes.html?ver=13) (steps 1–3).

1. Create a backup to tape job as described in the Veeam Backup & Replication User Guide, section [Creating Backup to Tape Jobs](https://tw-preview.dev.amust.local/html/vbr/13.0.1/userguide/creating_backup_to_tape_jobs.html?ver=13).

|  |
| --- |
| Note |
| You cannot restore oVirt VMs directly from tapes. To restore an oVirt VM, you must first restore its backups to a repository as described in the Veeam Backup & Replication User Guide, section [Backup Restore from Tape to Repository](https://tw-preview.dev.amust.local/html/vbr/13.0.1/userguide/vm_restore_from_tape_to_repository.html?ver=13). |

[![Backup to Tape Jobs](images/backup_to_tape.webp)](images/backup_to_tape.webp "Backup to Tape Jobs")


