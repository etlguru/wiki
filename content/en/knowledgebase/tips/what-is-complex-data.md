---
author: Maria Salter
title: What is Complex Data
description: This article describes transforming complex data
draft: false
tags: ['Knowledgebase', 'Complex Data']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

This Article provides examples of complex and simple data. We recommend using [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) for working with complex data structures and [Visual Importer ETL](https://www.etl-tools.com/visual-importer-etl-enterprise/overview.html) with simple, if in doubt please [contact us](https://www.etl-tools.com/contact-us.html) and we will [help you to choose](https://www.etl-tools.com/contact-us.html).

## Simple data example: Excel file

Data has a stable structure and there is only one value in the cell. Most database tables and delimited files can be considered as simple data. except when a single field has multiple values or holds xml data.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/simple-data.png" title="Excel file" >}}

## Simple XML file

XML tags are in the same order, the number of tags is always the same and there are no attributes, This XML does not require any additional transformation and can be easily loaded into the database.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/simple-xml.png" title="Simple XML file" >}}

## Complex XML message

The structure is not stable, the number of tags is different for a different customer record, plus it uses attributes. This XML may need some additional transformations.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/complex-xml.png" title="Complex XML message" >}}

## Complex Text file

Data is split between different rows some empty rows should be ignored, some data must be taken from the header

{{< image class="mx-auto d-block"  src="/images/knowledgebase/complex-text.png" title="Complex Text file" >}}

## SQL Insert script

Data can be easily extracted or generated using Advanced ETL Processor

{{< image class="mx-auto d-block"  src="/images/knowledgebase/insert-statement.png" title="SQL insert script" >}}

{{< aetl >}}
