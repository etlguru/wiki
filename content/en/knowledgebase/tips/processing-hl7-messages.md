---
author: Maria Salter
title: Processing HL7 Messages
description: This article describes how to configure Advanced ETL Processor for HL7 processing
draft: false
tags: ['Knowledgebase', 'HL7', 'Agent']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## General setting

{{< image class="mx-auto d-block"  src="/images/knowledgebase/hl71.png" title="General setting" >}}
/
{{< image class="mx-auto d-block"  src="/images/knowledgebase/hl72.png" title="General setting" >}}

## IP Address

The IP address of data reader must be the same as the computer it is being run on.\
Use ipconfig to get IP Address

{{< image class="mx-auto d-block"  src="/images/knowledgebase/hl73.png" title="IP Address" >}}
/
{{< image class="mx-auto d-block"  src="/images/knowledgebase/hl74.png" title="IP Address" >}}

## Executing transformation

Click plus\
Select transformation to run\
Enter correct computer name\
Select how often -> once

{{< image class="mx-auto d-block"  src="/images/knowledgebase/hl75.png" title="Executing transformation" >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/hl76.png" title="Executing transformation" >}}

To run HL7 Transformation Press the green arrow.
{{< alert color="secondary">}}Only one HL7 transformation can listen to the port at the same time.{{< /alert >}}

## Checking if transformation is running

{{< image class="mx-auto d-block"  src="/images/knowledgebase/hl77.png" title="Checking if transformation is running" >}}

Status must be running

## Stopping transformation

Check “Abort Execution” wait for the transformation to abort

## Making changes

To apply changes stop and start execution again.

## Performance considerations

Writing Thousands of HL7 messages into the same directory can slow down the process. \
Creating a new folder for every day or hour will help to keep performance high\
Disk space/database space usage must be constantly monitored

{{< aetl >}}
