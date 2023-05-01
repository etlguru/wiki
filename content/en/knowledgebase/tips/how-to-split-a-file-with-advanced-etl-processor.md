---
author: Maria Salter
title: How to split a file with Advanced ETL Processor
description: This article describes How to split a file with Advanced ETL Processor
draft: false
tags: ['Knowledgebase', 'Advanced ETL Processor', 'Transformation']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

One of the benefits of using Advanced ETL Processor is the ability to load data into multiple targets. Below is a list of customer's orders exported from a CRM system. There are two different kinds of records

## Source Data

- RECORD-TYPE=1 - Customer Details
- RECORD-TYPE=2 - Customer Orders

{{< image class="mx-auto d-block"  src="/images/knowledgebase/customer-orders-1.png" title="Source Data" >}}
\
You can actually load a list of customers and a list of orders into **two completely different databases**. In this example we use [Validator Object]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}}) and validation function "Is Equal To" to separate data flow.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/etl-splitting-files-2.png" title="Splitting Files" >}}

## List of Customers

{{< image class="mx-auto d-block"  src="/images/knowledgebase/etl-writer-customers-3.png" title="The Result of ETL Transformation - List of Customers" >}}

## List of Orders

{{< image class="mx-auto d-block"  src="/images/knowledgebase/etl-writer-orders-4.png" title="The Result of ETL Transformation - List of Orders" >}}

{{< aetl >}}
