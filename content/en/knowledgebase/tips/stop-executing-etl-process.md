---
author: Maria Salter
title: Stop executing ETL process
description: This article explains how to stop ETL process execution
draft: false
tags: ['Knowledgebase', 'Package', 'Execution']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

Quite often people ask us how to stop all ETL packages execution.

**“When I start Advanced ETL Processor it immediately runs transformation package. How can I avoid it?”**

{{< alert color="secondary" >}}Most of the time, this is because the Professional version is being used to execute the packages.{{< /alert >}}
\
A better option is to use Enterprise version agent and run tasks in parallel.

## To stop execution

- Close Advanced ETL Processor/Visual Importer ETL
- Click Start => DB Software Laboratory => Advanced ETL Processor Enterprise=> Advanced ETL Processor Enterprise Options=>Execution
- and Check **‘Do not execute any actions’**

## Options Dialogue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/options-execution.png" title="How to stop ETL process execution" >}}
\
The second option allows disabling execution remotely using SQL or Management Console

{{< image class="mx-auto d-block"  src="/images/knowledgebase/enable-scheduler.png" title="Enable Scheduler" >}}
\
This work for both Advanced ETL Processor and Visual Importer ETL

## Related forum posts:

- [Stopping Package Execution](https://www.etl-tools.com/forum/advanced-etl-processor/7218-stopping-package-execution)
- [Stop Executon](https://www.etl-tools.com/forum/advanced-etl-processor/7496-stop-execution#10099)

{{< aetl >}}
