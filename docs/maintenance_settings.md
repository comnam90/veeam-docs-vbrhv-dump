---
title: "Appendix A. Deprecated Functionality"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/maintenance_settings.html"
last_updated: "10/13/2025"
product_version: "13.7.0.473"
---

# Appendix A. Deprecated Functionality


Starting from version 7, Veeam Plug-in for OLVM and RHV comes without the backup appliance that was previously used to perform management operations, process jobs and deliver backup traffic. The functionality of backup appliance is now integrated into the backup server.

When upgrading to 7, you will be prompted to copy backup appliance configuration settings to the Veeam Backup & Replication configuration database. After the migration is complete, the backup appliance VM will be removed, and a worker will be deployed instead. For more information on on upgrading to 7, see [Upgrading to Veeam Plug-in for OLVM and RHV 7](upgrading.md).


