---
title: "Step 5. Define Job Schedule"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/backup_job_schedule.html"
last_updated: "10/20/2025"
product_version: "13.7.0.473"
---

# Step 5. Define Job Schedule


At the Schedule step of the wizard, you can instruct Veeam Plug-in for OLVM and RHV to start the backup job automatically according to a specific backup schedule. The backup schedule defines how often data of the VMs added to the backup job will be backed up.

Veeam Plug-in for OLVM and RHV allows you to create schedules of the following types:

* Daily at this time — the backup job will create restore points at a specific time on specific days.
* Monthly at this time — the backup job will create restore points once a month on a specific day.
* Periodically every — the backup job will create restore points repeatedly with a specific time interval every day.

|  |
| --- |
| Tip |
| You can instruct Veeam Plug-in for OLVM and RHV to run the backup job again if it fails on the first try. To do that, select the Retry failed items processing check box, and specify the maximum number of attempts to run the backup job and the time interval between retries. When retrying backup jobs, Veeam Plug-in for OLVM and RHV processes only those VMs that failed to be backed up during the previous attempt. |

![Step 5. Define Job Schedule](images/backup_job_add_schedule.webp "Select Restore Point")


