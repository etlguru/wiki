---
author: Peter Jonson
title: IMAP4 Monitor
description: Monitors IMAP4 server(s) for new email and execute actions
draft: false
tags: ['Automation', 'Monitor', 'IMAP4']
date: 2023-03-04
group: advanced-etl-processor-enterprise-monitors
menu: advanced-etl-processor-enterprise
layout: docs
---

The IMAP4 Monitor checks the IMAP4 server for new email messages.

- Multiple IMAP4 servers can be monitored
- Automatically performs user-defined tasks and actions.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors.png" title="IMAP4 Monitor" >}}

## Creating New Monitor

- To create a new Monitor select the "Event Monitors" tab and click New
- Dialog box will appear
- Fill in the Description edit box with the name of the Monitor you are about to create
- Select Email Message (IMAP4) as an event to monitor
- Change computer name if necessary
- Select IMAP4 connection to monitor from the drop-down box
- Switch to execute tab
- Select object to execute
- Change computer name if necessary
- Change application platform if necessary
- Click OK to finish the creation of the Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/imap4-monitor-1.png" title="Creating New Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/pop3-monitor-3.png" title="Creating New Monitor" >}}

## Installing IMAP4 Monitor

IMAP4 Monitor service is automatically installed during setup but not configured.

It can be also installed using the command line

To install the IMAP4 Monitor as a service run the following command:

{{< command >}}
aetlimap4monitor.exe /INSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpimap4monitor.exe /INSTALL
{{< /command >}}

for Visual Importer ETL

If the Monitor is already installed it must be uninstalled first

To uninstall the Monitor as a Windows service you must run the Monitor with the /UNINSTALL switch as follows

{{< command >}}
aetlimap4monitor.exe /UNINSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpimap4monitor.exe /UNINSTALL
{{< /command >}}

for Visual Importer ETL

The commands above must be executed as administrator (elevated).

## Configuring IMAP4 Monitor service

It is recommended to run IMAP4 Monitor using the same user used to design Packages/Transformations/SQL scripts.

- Open windows services
- IMAP4 Monitor in the list
- Double click on it
- Dialog box will appear
- Set startup time to automatic
- Change username
- Start the service

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/imap4-monitor-services.png" title="Configuring IMAP4 Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/imap4-monitor-service-1.png" title="Configuring IMAP4 Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/imap4-monitor-service-2.png" title="Configuring IMAP4 Monitor service" >}}

### Important Notes

IMAP4 Monitor is only available with Enterprise Version.

IMAP4 Monitor looks for new email messages to arrive (Works only when the number of messages goes up)

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

#### Action was submitted by IMAP4 Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/imap4-monitor-execution-log.png" title="Action was submitted by IMAP4 Monitor" >}}

### IMAP4 Monitor Variables

```
<Monitor ID>
```

{{< aetl >}}
