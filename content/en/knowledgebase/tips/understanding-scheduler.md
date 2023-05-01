---
author: Maria Salter
title: Understanding Scheduler
description: This article describes working with Scheduler
draft: false
tags: ['Knowledgebase', 'Scheduler', 'Agent']
date: 2022-08-01
group: knowledgebase-tips
layout: docs
---

## How to enable Scheduler

Scheduled actions can be executed by ETL Designer or by Execution Agent

Actions are Packages, Transformations, Import Scripts and SQL Scripts

### Executing Actions using ETL Designer

Be default scheduler execution is disabled.

To enable scheduler:

- Click File -> Options -> Execute tab and UnCheck "Do not execute any actions"
- Click maintenance and check enable

The second option allows disabling execution remotely using SQL or Management Console

{{< image class="mx-auto d-block"  src="/images/knowledgebase/enable-scheduler.png" title="Enable Scheduler" >}}

#### Options Dialogue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/options-execution.png" title="Options Dialogue" >}}

**Execute Actions in separate thread**

Prevents user interface from freezing, this option decreases performance

{{< alert color="secondary" >}}Keep Designer open all the time, otherwise, nothing will be executed{{< /alert >}}

### Executing Actions Using Execution Agent

Another way to execute the actions is to use the agent. The agent is windows service which is constantly running in the background. It executes actions automatically without user interaction.

To enable agent execution:

- Make sure that agent service is registered
- Start the agent service
- Select Maintenance Tab
- Enable Agent execution

{{< image class="mx-auto d-block"  src="/images/knowledgebase/01-options.png" title="Options" >}}

This option allows disabling execution remotely using SQL or Management Console

{{< image class="mx-auto d-block"  src="/images/knowledgebase/01-schedule.png" title="Schedule" >}}

#### Terminate on timeout

Timeout is approximate. Once the timeout is reached current action will terminate or stop executing and no further actions would be executed. This option only works with the agent.

#### Options Dialogue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/options-execution.png" title="Options Dialogue" >}}

**Execute One Action at the time**

Disables parallel execution so only one action is executed at the time. This option only works with the agent.

#### Avoiding problems

To avoid access issues with access right we always recommend using the actual user to run it.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/01-service.png" title="Service" >}}

Mapped drives do not exist in windows services world. Always use UNC path.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/01-directory.png" title="Directory" >}}

Use UNC path for logging.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/01-log.png" title="Log" >}}

## How Scheduler Works

When execution is enabled, there are two processes constantly running. One is checking schedule and if there is something to execute it adds the record to the queue. Another one is checking the queue and if it is not empty it executes the action.

Once the record is added to the queue scheduler calculates next time of execution.

Remember: Everything is related to the current time, right now is 16:00. If we schedule for execution at 15:00 it will be tomorrow’s date or if we schedule execution at 17:00 execution date will be today.

### Video Tutorials

{{< youtube id="h-XoeJnElig" class="ratio ratio-16x9" >}}
\
{{< youtube id="pPCrWKKGg1A" class="ratio ratio-16x9" >}}

{{< aetl >}}
