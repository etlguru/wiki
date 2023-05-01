---
author: Peter Jonson
title: Introduction
description: Visual Importer ETL Introduction
draft: false
tags: ['Introduction']
date: 2022-08-01
group: visual-importer-etl-enterprise
menu: visual-importer-etl-enterprise
weight: 1000
layout: docs
---

{{< alert color="danger" >}}
**Visual importer ETL** is the first ETL software product we created.
Since then we have designed **[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)** which is fully compatible with it and has much more features.\
For all new users we recommend **[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)**
{{< /alert >}}

[Visual Importer ETL](https://www.etl-tools.com/visual-importer-etl-standart/overview.html) is a Codeless ETL Tool. It has two major components Data import engine and Automation engine

## Import Example

Transformation engine converts data from one format into anther for example text file into excel file. Typical transformation consist of reader, validator, transformer and writer. Data flows from the left to the right.

{{< image class="mx-auto d-block"  src="/images/etl/visual-importer-etl/import-script-example.png" title="Visual Importer ETL Import Example" >}}

## Automation Example (Package)

Automation Package consist of actions. Action represent a single step of work. For example copy file or send email. Every package has a stating point. Action has two execution statuses Failure or Success. Once action execution is completed next action is executed depending on the execution status.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/introduction/automation-package-example.png" title="Visual Importer ETL Example" >}}
\
The best way to learn our ETL software is to watch video's. They are very shot and designed to explain one function. Documentation provides more detailed information.

{{< alert color="warning" >}}
Visual importer ETL is the first ETL software product we created.
Since then we have designed [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) which is fully compatible with it and has much more features.\
Most of Advanced ETL Processor videos are relevant to Visual Importer ETL except the ones describing how to work with transformations.
{{< /alert >}}

## Video Tutorial

{{< youtube id="ts676kkTR-Q" class="ratio ratio-16x9" >}}

{{< vimpe >}}
