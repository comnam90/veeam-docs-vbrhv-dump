---
title: "Step 2. Select Restore Point"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/restore_to_rhv_select_vms.html"
last_updated: "10/24/2025"
product_version: "13.7.0.473"
---

# Step 2. Select Restore Point


At the Virtual Machines step of the wizard, select a restore point that will be used to restore the selected VM. By default, Veeam Plug-in for OLVM and RHV uses the most recent valid restore point. However, you can restore the VM data to an earlier state.

To select a restore point, do the following:

1. Select the VM.
2. Click Point.
3. In the Restore Points window, select the necessary restore point and click OK.

To help you choose a restore point, Veeam Plug-in for OLVM and RHV provides the following information on each available restore point:

* Job — the name of the backup job that created the restore point and the date when the restore point was created.
* Type — the type of the restore point.
* Location — the repository where the restore point is stored.

![Step 2. Select Restore Point](images/restore_vm_rhv_add_vms.webp)


