---
author: Maria Salter
title: Understanding Transformation Metadata
description: Advanced ETL Processor metadata dialogue
draft: false
tags: ['Knowledgebase', 'Transformation', 'Metadata']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

The metatadata object can tell a lot about current transformation provided that it is used correctly
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/meta-data-transformation-properties.png" title="Meta Data Transformation Properties" >}}
\
Some values are only relevant to the reader which is currently being executed, for example, source file name or record number.

For those properties, it will work fine inside transformer TR 1 but since all data is already read after Sorter it will return incorrect data inside transformer TR 2

{{< image class="mx-auto d-block"  src="/images/knowledgebase/meta-data.png" title="Meta Data" >}}

{{< aetl >}}
