---
author: Peter Jonson
title: FTP Monitor
description: Monitor FTP Servers for new files arrivals
draft: false
tags: ['Automation', 'Monitor', 'FTP', 'SFTP']
date: 2023-03-04
group: advanced-etl-processor-enterprise-monitors
menu: advanced-etl-processor-enterprise
layout: docs
---

The Ftp Monitor checks FTP server directories for new files.

- Multiple FTP servers can be monitored
- Multiple Directories can be monitored
- Full support for Unicode
- Automatically performs user-defined tasks and actions.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors.png" title="FTP Monitor" >}}

## Creating New Monitor

- To create a new Monitor select the "Event Monitors" tab and click New
- Dialog box will appear
- Fill in the Description edit box with the name of the Monitor you are about to create
- Select file creation as an event to monitor
- Change computer name if necessary
- Select FTP connection to monitor from the drop-down box
- Switch to execute tab
- Select object to execute
- Change computer name if necessary
- Change application platform if necessary
- Switch to the parameters tab
- Fill in remote directory and mask
- Fill in a comment if required
- Click OK to finish the creation of a Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/ftp-monitor-1.png" title="Creating New Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/ftp-monitor-2.png" title="Creating New Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/ftp-monitor-3.png" title="Creating New Monitor" >}}

## Installing FTP Monitor

FTP Monitor service is automatically installed during setup but not configured.

It can be also installed using a command line

To install the FTP Monitor as a service run the following command:

{{< command >}}
aetlftpmonitor.exe /INSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpftpmonitor.exe /INSTALL
{{< /command >}}

for Visual Importer ETL

If the Monitor is already installed it must be uninstalled first

To uninstall the Monitor as a Windows service you must run the Monitor with the /UNINSTALL switch as follows

{{< command >}}
aetlftpmonitor.exe /UNINSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpftpmonitor.exe /UNINSTALL
{{< /command >}}

for Visual Importer ETL

The commands above must be executed as administrator (elevated).

## Configuring FTP Monitor service

It is recommended to run FTP Monitor using the same user used to design Packages/Transformations/SQL scripts.

- Open windows services
- FTP Monitor in the list
- Double click on it
- Dialog box will appear
- Set startup time to automatic
- Change username
- Start the service

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/ftp-monitor-services.png" title="Configuring FTP Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/ftp-monitor-service-1.png" title="Configuring FTP Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/ftp-monitor-service-2.png" title="Configuring FTP Monitor service" >}}

### Important Notes

- FTP Monitor is only available with Enterprise Version.
- FTP Monitor looks for files with the most recent modification date

### Checking Monitor Status

- Make sure that the monitor service is up and running
- Make sure that the monitor service is using the appropriate username and password
- Make sure that the monitor is enabled on the maintenance tab
- Make sure that the monitor is enabled on the Event monitors tab
- Make sure that the execution agent is configured properly

#### Monitor is enabled on Maintenance tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-maintenance.png" title="Monitor is enabled on Maintenance tab" >}}

#### Monitor is enabled on Event Monitors tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors-arrow.png" title="Monitor is enabled on Event Monitors tab" >}}

#### Action was submitted by FTP Monitor

- {{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/ftp-monitor-execution-log.png" title="Action was submitted by FTP Monitor" >}}

### FTP Monitor Variables

```
<Monitor ID>
<FTP Monitor File Name>
<FTP Monitor Modification Date>
```

{{< aetl >}}
