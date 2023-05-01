---
author: Peter Jonson
title: Directory Monitor
description: Directory Monitor is a windows service which tracks folder changes, such as file creation, removal, modification or renaming.
draft: false
tags: ['Automation', 'Monitor']
date: 2023-03-04
group: advanced-etl-processor-enterprise-monitors
menu: advanced-etl-processor-enterprise
layout: docs
---

Directory Monitor is a windows service which tracks folder changes, such as file creation, removal, modification or renaming.

- Multiple locations can be monitored
- Network shares can be monitored using the UNC path
- Automatically performs user-defined tasks and actions.

## User Interface

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-1.png" title="Directory Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-2.png" title="Directory Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-3.png" title="Directory Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors.png" title="Event Monitor" >}}

## Installing Directory Monitor

Directory Monitor service is automatically installed during setup but not configured.

It can be also installed using the command line

To install the Directory Monitor as a service run the following command:

{{< command >}}
aetldirectorymonitor.exe /INSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpdirectorymonitor.exe /INSTALL
{{< /command >}}

for Visual Importer ETL

If the Monitor is already installed it must be uninstalled first

To uninstall the Monitor as a Windows service you must run the Monitor with the /UNINSTALL switch as follows

{{< command >}}
aetldirectorymonitor.exe /UNINSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpdirectorymonitor.exe /UNINSTALL
{{< /command >}}

for Visual Importer ETL

The commands above must be executed as administrator (elevated).

## Configuring Directory Monitor service

It is recommended to run Directory Monitor using the same user used to design packages/transformations/sql scripts.

- Open windows services
- Find Directory Monitor in the list
- Double click on it
- Dialog box will appear
- Set startup time to automatic
- Change username
- Start the service

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-services.png" title="Directory Monitor Services" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-service-1.png" title="Directory Monitor Service" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-service-2.png" title="Directory Monitor Service" >}}

### Checking Monitor Status

- Make sure that the monitor service is up and running
- Make sure that the monitor service is using the appropriate username and user
- Make sure that the user has access to directories monitored
- Make sure that the monitor is enabled on the maintenance tab
- Make sure that the directory is enabled on the Event monitors tab
- Make sure that the execution agent is configured properly

### Monitor is enabled on Maintenance tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-maintenance.png" title="Maintenance tab" >}}

### Monitor is enabled on Event Monitors tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors-arrow.png" title="Event Monitors tab" >}}

### Action was submitted by Directory Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/directory-monitor-execution-log.png" title="Action was submitted by Directory Monitor" >}}

### Directory Monitor Variables

```
<Monitor ID>
<Directory Monitor File Name>
```

## Things to Consider

- Directory Monitor is only available with Enterprise Version.
- Do not use mapped drives, use UNC path instead.
- "Wait until the file is ready" only works for file creation.
- What if you have 1000+ files copied into the directory? The directory monitor will fire a trigger for every single file

The solution to this problem is to use a trigger file.
Eg you copy 1000+ files into the directory and copy the last file called trigger.txt.
Set monitor mask to trigger.txt.
Monitor fires only once.
The package moves files into the different directories (with a timestamp) and processes the files one by one.

## Video Tutorial

{{< youtube id="RL41A-btZPk" class="ratio ratio-16x9" >}}

{{< aetl >}}
