---
author: Maria Salter
title: Things to avoid while designing data transformations
description: This Article describes Things to avoid while designing data transformations
draft: false
tags: ['Knowledgebase', 'Transformation', 'Tips']
date: 2023-03-14
group: knowledgebase-issues
layout: docs
---

- When a transformer is connected to the data writer it takes the list of fields from the data writer, transformation below will work only if the list of fields from both data writers is exactly the same
  \
  {{< image class="mx-auto d-block"  src="/images/knowledgebase/avoid1.png" title="Things to avoid while designing data transformations" >}}

- There is no need to sort data before using Joiner
  \
  {{< image class="mx-auto d-block"  src="/images/knowledgebase/avoid2.png" title="Things to avoid while designing data transformations" >}}

- The last object before data writer must be always data transformer {{< image class="mx-auto d-block"  src="/images/knowledgebase/avoid3.png" title="Things to avoid while designing data transformations" >}}

- When log object is present inside data transformation all log messages go through it. all validator and transformer objects must have "Write Message to Log File" and "Write Record to Rejected File" must be unchecked
  \
  {{< image class="mx-auto d-block"  src="/images/knowledgebase/avoid41.png" title="Things to avoid while designing data transformations" >}}
  \
  {{< image class="mx-auto d-block"  src="/images/knowledgebase/avoid42.png" title="Things to avoid while designing data transformations" >}}

{{< aetl >}}
