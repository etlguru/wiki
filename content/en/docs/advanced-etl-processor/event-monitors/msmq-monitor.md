---
author: Peter Jonson
title: MSMQ Monitor
description: Monitors MSMQ server(s) for new messages and execute actions
draft: false
tags: ['Automation', 'Monitor', 'MQTT']
date: 2023-03-04
group: advanced-etl-processor-enterprise-monitors
menu: advanced-etl-processor-enterprise
layout: docs
---

The MSMQ Monitor checks Message Queue (MSMQ) for new messages.

- Multiple Queues can be monitored
- Automatically performs user-defined tasks and actions.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors.png" title="Event Monitor" >}}

## Creating New Monitor

- To create a new Monitor select the "Event Monitors" tab and click New
- Dialog box will appear
- Fill in the Description edit box with the name of the Monitor you are about to create
- Select Message (MSMQ) as an event to monitor
- Change computer name if necessary
- Select MSMQ connection to monitor from the drop-down box
- Switch to execute tab
- Select object to execute
- Change computer name if necessary
- Change application platform if necessary
- Click OK to finish the creation of the Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/msmq-monitor-1.png" title="Creating New MSMQ Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/pop3-monitor-3.png" title="Creating New MSMQ Monitor" >}}

## Installing MSMQ Monitor

MSMQ Monitor service is automatically installed during setup but not configured.

It can be also installed using the command line

To install the MSMQ Monitor as a service run the following command:

{{< command >}}
aetlmsmqmonitor.exe /INSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpmsmqmonitor.exe /INSTALL
{{< /command >}}

for Visual Importer ETL

If the Monitor is already installed it must be uninstalled first

To uninstall the Monitor as a Windows service you must run the Monitor with the /UNINSTALL switch as follows

{{< command >}}
aetlmsmqmonitor.exe /UNINSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpmsmqmonitor.exe /UNINSTALL
{{< /command >}}

for Visual Importer ETL

The commands above must be executed as administrator (elevated).

## Configuring MSMQ Monitor service

It is recommended to run MSMQ Monitor using the same user used to design Packages/Transformations/SQL scripts.

- Open windows services
- Find MSMQ Monitor in the list
- Double click on it
- Dialog box will appear
- Set startup time to automatic
- Change user name
- Start the service

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/msmq-monitor-services.png" title="Configuring MSMQ Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/msmq-monitor-service-1.png" title="Configuring MSMQ Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/msmq-monitor-service-2.png" title="Configuring MSMQ Monitor service" >}}

### Important Notes

- MSMQ Monitor is only available with Enterprise Version.
- MSMQ Monitor assumes that Message Queue should be always empty.
- When it is not empty it records the arrival time of the first message.
- When the arrival time of the first message changes it fires the event.
- (It happens when some software removes all messages and a new message arrives)

### Checking Monitor Status

- Make sure that the monitor service is up and running
- Make sure that the monitor service is using the appropriate user name and user
- Make sure that the monitor is enabled on the maintenance tab
- Make sure that the monitor is enabled on the Event monitors tab
- Make sure that the execution agent is configured properly

#### Monitor is enabled on Maintenance tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-maintenance.png" title="Monitor is enabled on Maintenance tab" >}}

#### Monitor is enabled on Event Monitors tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors-arrow.png" title="Monitor is enabled on Event Monitors tab" >}}

#### Action was submitted by MSMQ Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/pop3-monitor-execution-log.png" title="Action was submitted by MSMQ Monitor" >}}

### MSMQ Monitor Variables

```
<Monitor ID>
```

{{< aetl >}}
