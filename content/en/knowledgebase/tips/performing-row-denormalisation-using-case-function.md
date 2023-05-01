---
author: Maria Salter
title: Performing Row Denormalisation using Case function
description: This article demonstrates how to de-normalize data by looking up key-value pairs
draft: false
tags: ['Knowledgebase', 'Case']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

This example demonstrates how to de-normalize data by looking up key-value pairs.

## Source Data:

{{< table "table-striped table-bordered" >}}

| ClientID  | Key   | Value   |
| --------- | ----- | ------- |
| ClientID1 | Name  | Bill    |
| ClientID1 | Phone | 1234567 |
| ClientID2 | Name  | Mark    |
| ClientID2 | Phone | 123456  |

{{< /table >}}

## Desired Result

{{< table "table-striped table-bordered" >}}

| ClientID  | Name | Phone   |
| --------- | ---- | ------- |
| ClientID1 | Bill | 1234567 |
| ClientID2 | Mark | 123456  |

{{< /table >}}

## Transformation

{{< image class="mx-auto d-block"  src="/images/knowledgebase/data-transformation.png" title="Transformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/case-statement-example.png" title="Case Statement" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/case-properties.png" title="Case Properties" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/grouper-properties.png" title="Grouper Properties" >}}
\
{{< alert color="secondary" >}}The beauty of the "Case" function is its incredible flexibility,
The data can be redirected in many ways using multiple criteria, that reduces clutter and makes it easy to understand complex ETL processes{{< /alert >}}

{{< aetl >}}
