---
author: Peter Jonson
title: Execution Log
description: Execution Log
draft: false
tags: ['Automation', 'Log']
date: 2022-09-24
group: advanced-etl-processor-enterprise-execution-automation
menu: advanced-etl-processor-enterprise
layout: docs
---

Once Package, Transformation or SQL Script (Action) is running or completed the Execution Monitor screen allows checking status or troubleshooting if any error happens.

The Action may have four different statuses:

- Executing
- Submitted
- Failed
- Finished

The log screen consists of two panels.

The **Top panel** shows the overall status of the execution.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/execution-monitor.png" title="Log screen " >}}\

{{< alert color="secondary" >}}
Double click on the top panel to see the log.
{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/execution-log.png" title="The log" >}}
\
The **Bottom panel** shows the status of individual items within the Package.
Double click on the Bottom panel to check item log.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/execution-log-viewer.png" title="Execution Log Viewer" >}}

## Toolbar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/execution-monitor-toolbar.png" title="Execution Log Toolbar" >}}

1. Shows Log dialogue
1. Refreshes the screen
1. Post changes
1. Deletes the record
1. Prints
1. Previews Grid
1. Find Record
1. Export Grid
1. Export Data into Excel
1. Show/Hide Fields
1. Auto format grid
1. Show grouping panel
1. Delete all records from the log (except the ones being executed right now)
1. Stops Execution
1. Show/Hides bottom panel
1. Refresh log every minute
1. Show first 10 records only
1. Open directory containing log files
1. Edit selected object

## Stopping Execution

The user can stop execution at any time by pressing {{< image src="/images/etl/advanced-etl-processor/execution-stop-icon.png" title="Stop Execution Button" >}}

{{< alert color="secondary" >}}
SQL script stops once execution of current SQL statement is finished. It could take some time to do.
{{< /alert >}}

{{< aetl >}}
