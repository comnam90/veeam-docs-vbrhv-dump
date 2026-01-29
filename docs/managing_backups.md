---
title: "Managing Backups"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/managing_backups.html"
last_updated: "3/7/2024"
product_version: "13.7.0.473"
---

# Managing Backups


Veeam Plug-in for OLVM and RHV stores information on all protected oVirt VMs in the configuration database. Even if a VM is no longer protected by any configured backup job and even if the VM no longer exists in the oVirt KVM environment, records about created backups will not be deleted from the database until Veeam Plug-in for OLVM and RHV automatically removes all restore points associated with this VM according to the retention settings saved in the backup metadata. You can manage oVirt VM backups as long as their records are present in the configuration database.

In This Section

* [Viewing Backup Properties](view_backup_properties.md)
* [Verifying Backups](verify_backups.md)
* [Exporting Backups](export_backups.md)
* [Copying Backups](backup_copy_job.md)
* [Copying Backups to Tapes](backup_tape_jobs.md)
* [Deleting Backups](retention.md)


