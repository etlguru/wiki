---
author: Maria Salter
title: Data Synchronization part 3
description: Data Synchronization article part 3
draft: false
tags: ['Knowledgebase', 'Synchronization']
date: 2023-03-28
group: knowledgebase-tips
layout: docs
---

In [Data Synchronization Part 2]({{<ref "data-synchronization-part-2" >}}) we demonstrated how easy it is to synchronize the data between different databases.

Both of the methods suggested works very well for small and medium-sized tables

For large tables, we must use a different approach. The basic idea is very simple we must work only with the relevant data.

In order to achieve that we must store and use maximum values of the primary key before and after the transformation

## Example

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-package-1.png" title="Synchronization" >}}

### Start value

The following SQL is used to get a starting point for the data reader, table PK_STATISTICS is used to store values.

### Table creation script

```sql
TABLE [dbo].[PK_STATISTICS]
([TABLE_NAME] [varchar](50) NULL,
[PK_BEFORE] [int] NOT NULL,
[PK_AFTER] [int] NOT NULL
)
ON [PRIMARY]
```

**1234567890** is a variable name, later inside data writer variable is replaced with the actual value

Variable Name can be any combination of characters

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-s1-2.png" title="Synchronization" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-package-variables1-3.png" title="Package Variables" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-package-variables2-4.png" title="Package Variables" >}}

### Transformation

Does actual loading

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-5.png" title="Transformation" >}}

### Reader

Reads new records from the source table using the following SQL

Variable **1234567890** is replaced with an actual value before the execution

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-datareader1-7.png" title="Reader" >}}

### Transformer

Just passes values to data writer

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-transformer1-8.png" title="Transformer" >}}

### Writer 1

Adds new records

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization2-writer1-9.png" title="Writer" >}}

SQL executed before the writer starts loading records

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-writer11-10.png" title="SQL" >}}

SQL executed once the writer finishes loading records

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-writer12-11.png" title="SQL" >}}

### Variables

Here we assign values to 1111111111111 and 9999999999 variables

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-s2-12.png" title="Variables" >}}

### Set Flag

Updates records in source table

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-setflag-13.png" title="Set Flag" >}}

Variables values

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization3-package-variables-14.png" title="Variables values" >}}

{{< aetl >}}
