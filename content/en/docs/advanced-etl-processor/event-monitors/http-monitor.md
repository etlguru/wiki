---
author: Peter Jonson
title: HTTP Monitor
description: HTTP server monitoring, Execute actions when the link is clicked
draft: false
tags: ['Automation', 'Monitor', 'http', 'webhook']
date: 2023-03-04
group: advanced-etl-processor-enterprise-monitors
menu: advanced-etl-processor-enterprise
layout: docs
---

The HTTP Monitor is a web server which executes an action when a predefined URL is open.

- Multiple HTTP ports or URLs can be monitored
- Automatically performs user-defined tasks and actions.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/event-monitors.png" title="HTTP Monitor" >}}

## Creating New Monitor

- To create a new Monitor select the "Event Monitors" tab and click New
- Dialog box will appear
- Fill in the Description edit box with the name of the Monitor you are about to create
- Select HTTP Request as an event to monitor
- Change computer name if necessary
- Select HTTP connection to monitor from the drop-down box
- Switch to execute tab
- Select object to execute
- Change computer name if necessary
- Change application platform if necessary
- Switch to the parameters tab
- Enter URL to check
- Click OK to finish the creation of the Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/http-monitor-1.png" title="Creating New Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/pop3-monitor-3.png" title="Creating New Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/http-monitor-3.png" title="Creating New Monitor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/tcpip-connection.png" title="Creating New Monitor" >}}

URL to use: [http://localhost:9000/startpackage.html](http://localhost:9000/startpackage.html)

## Installing HTTP Monitor

HTTP Monitor service is automatically installed during setup but not configured.

It can be also installed using the command line

To install the HTTP Monitor as a service run the following command:

{{< command >}}
aetlhttpmonitor.exe /INSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimphttpmonitor.exe /INSTALL
{{< /command >}}

for Visual Importer ETL

If the Monitor is already installed it must be uninstalled first

To uninstall the Monitor as a Windows service you must run the Monitor with the /UNINSTALL switch as follows

{{< command >}}
aetlhttpmonitor.exe /UNINSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimphttpmonitor.exe /UNINSTALL
{{< /command >}}

for Visual Importer ETL

The commands above must be executed as administrator (elevated).

## Configuring HTTP Monitor service

It is recommended to run HTTP Monitor using the same user used to design Packages/Transformations/SQL scripts.

- Open windows services
- Find HTTP Monitor in the list
- Double click on it
- Dialog box will appear
- Set startup time to automatic
- Change user name
- Start the service

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/http-monitor-services.png" title="Configuring HTTP Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/http-monitor-service-1.png" title="Configuring HTTP Monitor service" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/http-monitor-service-2.png" title="Configuring HTTP Monitor service" >}}

### Important Notes

HTTP Monitor is only available with Enterprise Version.

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

#### Action was submitted by HTTP Monitor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/windows-services/http-monitor-execution-log.png" title="Action was submitted by HTTP Monitor" >}}

### HTTP Monitor Variables

```
<Monitor ID>
```

{{< aetl >}}
