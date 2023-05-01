---
author: Peter Jonson
title: Introduction
description: Advanced ETL Processor Introduction
draft: false
tags: ['Transforming Data', 'Introduction']
date: 2022-08-01
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
weight: 1000
layout: docs
---

[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) is a Codeless ETL Tool. It has two major components Data transformation engine and Automation engine

## Transformation Example

Transformation engine converts data from one format into anther for example text file into excel file. Typical transformation consist of reader, validator, transformer and writer. Data flows from the left to the right.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/introduction/transformation-example.png" title="Advanced ETL Processor Transformation Example" >}}

## Automation Example (Package)

Automation Package consist of actions. Action represent a single step of work. For example copy file or send email. Every package has a stating point. Action has two execution statuses Failure or Success. Once action execution is completed next action is executed depending on the execution status.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/introduction/automation-package-example.png" title="Advanced ETL Processor Example" >}}
\
The best way to learn our ETL software is to watch video's. They are very shot and designed to explain one function. Documentation provides more detailed information.

- For all new users, we recommend watching [02 Getting familiar with the user interface](https://www.etl-tools.com/tutorials/02-getting-familiar-with-user-interface.html)
- If your main goal is transforming the data watch [10 Creating basic ETL Transformation](https://www.etl-tools.com/tutorials/10-creating-basic-etl-transformation.html)
- If you want to start automating your business watch [11 Creating Packages](https://www.etl-tools.com/tutorials/11-creating-packages.html)
- [How to connect guides]({{<relref "/knowledgebase/connections/" >}})

Please also watch the repository videos. Understanding working with the repository is extremely important.

## Video Tutorial

{{< youtube id="j-sNUMrUn30" class="ratio ratio-16x9" >}}

{{< aetl >}}
