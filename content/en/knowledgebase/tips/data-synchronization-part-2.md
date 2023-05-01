---
author: Maria Salter
title: Data Synchronization part 2
description: Data Synchronization article part 2
draft: false
tags: ['Knowledgebase', 'Synchronization']
date: 2022-07-14
group: knowledgebase-tips
layout: docs
---

In [Data Synchronization Part 1]({{<ref "data-synchronization-part-1" >}}) we demonstrated how easy it is to synchronize the data between different databases.

The proposed approach has some disadvantages

Writer 1 may put too much pressure on the target database

for every incoming record runs the following SQL

```sql
select count(*) as rec_count from target table where PRIMARY_KEY=?
```

if rec_count is zero a new record is inserted into the target table"

## Here is an alternative approach

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization2-1.png" title="Synchronization" >}}

### Reader

Reads new records from the source table using the following SQL

```sql
Select
TBL_SOURCE.PRIMARY_KEY,
TBL_SOURCE.DATA,
TBL_SOURCE.UPDATE_FLAG
From
TBL_SOURCE
Where
TBL_SOURCE.UPDATE_FLAG = 'N'
```

### Validator

Checks if the record exists in the database and it does discard it

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization2-validator1-2.png" title="Synchronization Validator" >}}
\
**Is In list** validation function pools list of primary key values and builds the tree in the memory, this is a very fast and efficient way to validate data

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization2-isinlist1-3.png" title="Synchronization InList" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization2-isinlist2-4.png" title="Synchronization InList" >}}

### Transformer 1

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-transformer1-5.png" title="Synchronization Transformer" >}}

**Writer 1**

Adds new record

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization2-writer1-6.png" title="Synchronization Writer" >}}

Once loading is completed the following SQL is executed to mark processed records in the target table.

```sql
update TBL_TARGET
SET UPDATE_FLAG='Y'
WHERE UPDATE_FLAG='N'
```

Using this approach allows easy identification of newly inserted records in case of failure

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-writer11-7.png" title="Synchronization Writer" >}}

### Sorter

Sorter is used to delay passing records to writer 2 until writer 1 is completed

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-sorter-8.png" title="Synchronization Sorter" >}}

### Transformer 2

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-transformer2-9.png" title="Synchronization Transformer" >}}

### Writer 2

Updates records in the source table

```sql
update TBL_SOURCE
SET UPDATE_FLAG = 'Y'
where PRIMARY_KEY=?
```

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-writer2-10.png" title="Writer" >}}

[Data Synchronization Part 3]({{<ref "data-synchronization-part-3" >}})

{{< aetl >}}
