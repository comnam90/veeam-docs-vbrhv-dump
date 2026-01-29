---
title: "Testing Workers"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/rhv_workers_test.html"
last_updated: "11/24/2025"
product_version: "13.7.0.473"
---

# Testing Workers


Before using a worker for a backup or restore operation, Veeam Backup & Replication automatically tests its configuration — verifies that the worker service can start successfully, checks that the worker can connect to the backup server and to the cluster, and installs available updates.

If you want to ensure that the worker configuration is correct before it is used for a backup or restore operation, you can start a worker configuration test manually:

1. Open the Backup Infrastructure view.
2. In the inventory pane, select Backup Proxies.
3. In the working area, select the necessary worker and click Test Worker on the ribbon.
4. Alternatively, right-click the worker and select Test.

[![Testing Workers](images/testing_workers.webp)](images/testing_workers.webp "Testing Workers")


