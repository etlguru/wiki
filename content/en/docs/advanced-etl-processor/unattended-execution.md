---
author: Peter Jonson
title: Execution Automation
description: This article describes services dedicated to ETL process execution and automation
draft: false
tags: ['Automation', 'Unattended Execution']
date: 2022-09-28
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

Enterprise Version offers various windows services dedicated to unattended execution.

## Execution Flow

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/execution-flow.png" title="Execution Flow" >}}

The execution flow above is based on microservices architecture. Its main benefit of it is resilience. If one component fails the rest will continue working. Components can be updated independently or moved from server to server

**Notes:**

- When an event happens event monitor inserts a record into the execution queue.
- Scheduler is constantly checking the schedule table and if there's something to execute it inserts a record into the execution queue
- Execution agent is constantly checking queue table and if there's something to execute it launches command line execution utility
- Once the command line execution utility completes the execution it moves records from the queue table into queue_archive
- Scheduler is a part of the execution agent

## [Execution Automation]({{<relref "docs/advanced-etl-processor/automation" >}})

- [Using Command Line Interface]({{<relref "docs/advanced-etl-processor/automation/command-line-interface" >}})
- [Scheduler]({{<relref "docs/advanced-etl-processor/automation/scheduler" >}})
- [Execution Log]({{<relref "docs/advanced-etl-processor/automation/execution-log" >}})
- [Execution Agent]({{<relref "docs/advanced-etl-processor/automation/execution-agent" >}})

## [Event Monitors]({{<relref "docs/advanced-etl-processor/automation/event-monitors" >}})

- [Directory Monitor]({{<relref "docs/advanced-etl-processor/event-monitors/directory-monitor" >}})
- [FTP Monitor]({{<relref "docs/advanced-etl-processor/event-monitors/ftp-monitor" >}})
- [POP3 Monitor]({{<relref "docs/advanced-etl-processor/event-monitors/pop3-monitor" >}})
- [IMAP4 Monitor]({{<relref "docs/advanced-etl-processor/event-monitors/imap4-monitor" >}})
- [Office 365 Monitor]({{<relref "docs/advanced-etl-processor/event-monitors/office365-monitor" >}})
- [MSMQ Monitor]({{<relref "docs/advanced-etl-processor/event-monitors/msmq-monitor" >}})
- [HTTP Monitor]({{<relref "docs/advanced-etl-processor/event-monitors/http-monitor" >}})

## Video Tutorials

{{< youtube id="RSvg-zy3sQA" class="ratio ratio-16x9" >}}
\
{{< youtube id="h_XoeJnElig" class="ratio ratio-16x9" >}}
\
{{< youtube id="pPCrWKKGg1A" class="ratio ratio-16x9" >}}
\
{{< youtube id="RL41A-btZPk" class="ratio ratio-16x9" >}}
\
{{< youtube id="Q814WexRfDs" class="ratio ratio-16x9" >}}

{{< aetl >}}
