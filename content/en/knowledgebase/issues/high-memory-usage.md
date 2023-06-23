---
author: Maria Salter
title: High Memory Usage
description: High Memory Usage, Unresponsive Server
draft: false
tags: ['Knowledgebase', 'Performance']
date: 2023-03-14
group: knowledgebase-issues
layout: docs
---

Number of customers complained to us about sudden problems with performance

## Background

Package runs every five minutes and it takes 1 minute to complete  
Agent is used for execution

## Issue

Source database server fails and execution get stuck or packages block each other

- After one hour we have 12 aetlcl.exe stuck
- After 24 hours we have 288 aetlcl.exe stuck
- Eventually the server becomes unresponsive

{{< image class="mx-auto d-block"  src="/images/knowledgebase/high-memory-usage-task-manager.png" title="Task Manager" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/high-memory-usage-execution-log.png" title="Execution Log" >}}

## Solution for the problem

Set Terminate on timeout

{{< image class="mx-auto d-block"  src="/images/knowledgebase/high-memory-usage-terminate-on-timeout.png" title="Terminate on timeout" >}}

Set Execute one action at the time

{{< image class="mx-auto d-block"  src="/images/knowledgebase/high-memory-usage-execute-one-action-at-the-time.png" title="Task Manager" >}}

{{< aetl >}}
