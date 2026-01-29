---
title: "Considerations and Limitations"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/limitations_rhv.html"
last_updated: "11/24/2025"
product_version: "13.7.0.473"
---

# Considerations and Limitations


Backup

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization does not support creation of application-consistent backups.

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization only supports the following virtual disk formats for VM backup: RAW and QCOW2.

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization enables deduplication and applies 1MB block size setting for all VM backups by default. These settings cannot be changed.

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization supports VM backup operations with one backup job per VM at a time. If a VM is already being processed by a backup job, another backup job will not start processing this VM until the currently running backup operation completes.

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization cannot run a VM backup operation for a VM that already has a restore operation running. Wait for the restore process to complete, and then start the backup job.

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization does not support backup of hosted-engine VMs. However, you can create a backup of the oVirt configuration. For more information, see [Red Hat Virtualization documentation](https://access.redhat.com/documentation/en-us/red_hat_virtualization/4.4/html-single/administration_guide/index#chap-Backups_and_Migration) or [Oracle Linux Virtualization Manager documentation](https://docs.oracle.com/en/virtualization/oracle-linux-virtualization-manager/admin/admin-vm-tasks.html#LVMAD-vm-snapshot-create-top).

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization cannot run a backup operation for a VM that already has a snapshot preview operation running. For more information, see [Red Hat Virtualization documentation](https://access.redhat.com/documentation/en-us/red_hat_virtualization/4.4/html/technical_reference/snapshot_previews) or [Oracle Linux Virtualization Manager documentation](https://docs.oracle.com/en/virtualization/oracle-linux-virtualization-manager/admin/admin-admin-tasks.html#vm-snapshot-create-top).

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization does not support backup of VMs with [shareable disks](https://www.ovirt.org/documentation/administration_guide/index.html#Shareable_Disks) or [direct LUN disks](https://www.ovirt.org/documentation/administration_guide/index.html#sect-Virtual_Disk_Tasks) attached.

Veeam Plug-in for Oracle Linux Virtualization Manager and Red Hat Virtualization does not support addition to the backup scope for VMs that are being backed up by 3rd party software. Wait for the backup process to complete or stop the currently running job manually, and then add the VM to the necessary backup job.

By default, [backup encryption](https://helpcenter.veeam.com/docs/vbr/userguide/data_encryption.html?ver=13) is disabled for backed-up data. However, you can enable encryption at the repository level. For more information, see the Veeam Backup & Replication User Guide, section [Access Permissions](https://helpcenter.veeam.com/docs/vbr/userguide/access_permissions.html?ver=13).

[VM guest OS file indexing](https://helpcenter.veeam.com/docs/vbr/userguide/indexing.html?ver=13) is not supported for backups created with Veeam Plug-in for OLVM and RHV.

Since Veeam Backup & Replication does not allow you to assign [information about locations](https://helpcenter.veeam.com/docs/vbr/userguide/locations.html?ver=13) to the oVirt KVM Manager, job statistics do not include information on the oVirt VM data migration between different geographic regions.

If you want to back up a VM that has been configured with a [oVirt KVM Virtualization Cloud-Init custom script](https://access.redhat.com/documentation/ru-ru/red_hat_virtualization/4.0/html/virtual_machine_management_guide/sect-using_cloud-init_to_automate_the_configuration_of_virtual_machines#doc-wrapper), first remove the script from the VM since it may contain secure data (such as credentials and authorized keys) that will appear in Veeam Plug-in for OLVM and RHV backup logs.


