---
author: Peter Jonson
title: Execution Agent
description: The Execution Agent is a Microsoft Windows service which automatically executes scheduled actions such as Packages, Transformations, Imports and SQL scripts
draft: false
tags: ['Automation', 'Execution Agent', 'Schedule']
date: 2022-09-28
group: advanced-etl-processor-enterprise-execution-automation
menu: advanced-etl-processor-enterprise
layout: docs
---

The Execution Agent is a Microsoft Windows service that automatically executes scheduled actions such as packages, transformations, imports and SQL scripts.

{{< alert color="secondary" >}}
Execution Agent is only available with Enterprise Version.
{{< /alert >}}

## Installing Execution Agent

The Execution Agent can be installed using the command line or via the user interface.

To install the Execution Agent as a service run the following command:

{{< command >}}
aetlagent.exe /INSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpagent.exe /INSTALL
{{< /command >}}

for Visual Importer ETL

If the agent is already installed it must be uninstalled first

To uninstall the Execution Agent as a Windows service you must run the Agent with the /UNINSTALL switch as follows

{{< command >}}
aetlagent.exe /UNINSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vimpagent.exe /UNINSTALL
{{< /command >}}

{{< alert color="secondary" >}}
The commands above must be executed as administrator (elevated).\
The agent works once the license key is installed.\
The agent is automatically installed during setup but not configured.\
64-bit execution can execute both 64-bit and 32-bit actions\
It is recommended to run Execution Agent using the same user you use to design actions.\
Do not use mapped drives, use the UNC path instead
{{< /alert >}}

### Checking Agent Status

### Agent Email Notifications

Another way to control Agent status is through email notifications

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/execution-agent-notifications.png" title="Execution Agent Email Notifications" >}}

## Useful Links

- [Understanding Scheduler]({{<relref "/knowledgebase/tips/understanding-scheduler" >}})

## Video Tutorial

{{< youtube id="pPCrWKKGg1A" class="ratio ratio-16x9" >}}

{{< aetl >}}
