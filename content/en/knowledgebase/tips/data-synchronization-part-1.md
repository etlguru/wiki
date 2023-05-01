---
author: Maria Salter
title: Data Synchronization part 1
description: This article was created to assist our customers with data synchronization.
draft: false
tags: ['Knowledgebase', 'Synchronization']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

This article was created to assist our customers with data synchronization.

In our examples we will be synchronizing between different physical SQL servers, the same methodology can be used for any database

**Here is table creation script**

```sql
CREATE TABLE TBL_SOURCE
(
PRIMARY_KEY int NOT NULL IDENTITY (1,1),
DATA varchar(50) NULL,
UPDATE_FLAG varchar(5) NULL
) ON
[PRIMARY]
GO
ALTER TABLE TBL_SOURCE ADD CONSTRAINT
PK_TBL_SOURCE PRIMARY KEY CLUSTERED
(PRIMARY_KEY) WITH( STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF,
ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON
[PRIMARY]
GO
CREATE TABLE TBL_TARGET
(PRIMARY_KEY int NOT NULL,
DATA varchar(50) NULL,
UPDATE_FLAG varchar(5) NULL
) ON
[PRIMARY]
GO
ALTER
TABLE TBL_TARGET ADD CONSTRAINT
PK_TBL_TARGET PRIMARY KEY CLUSTERED
(PRIMARY_KEY)
WITH( STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON
[PRIMARY]
GO
```

## Objective

- Load new records only into target table
- Once loading is completed source records must be marked as updated

## Assumptions

- Data is only inserted into source table
- There are no changes to the source records
- There are no deletions to the source records

## Implementation

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1.png" title="Synchronization" >}}

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

### Transformer 1

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-transformer1-2.png" title="Synchronization Transformer" >}}

### Writer 1

Adds new records only

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-writer1-3.png" title="Synchronization Writer" >}}

for every incoming record runs the following SQL

```sql
select count(*) as rec_count from target table where PRIMARY_KEY=?
```

if rec_count is zero new records is inserted into the target table

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-udatekey1-4.png" title="Update Key" >}}

Once loading is completed the following SQL is executed to mark processed records in the target table.

```sql
update TBL_TARGET
SET UPDATE_FLAG='Y'
WHERE UPDATE_FLAG='N'
```

Using this approach allow easy identification of newly inserted records in case of failure

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-writer11-5.png" title="Synchronization Writer" >}}

### Sorter

Sorter is used to delay passing records to writer 2 until writer 1 is completed

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-sorter-6.png" title="Synchronization Sorter" >}}

### Transformer 2

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-transformer2-7.png" title="Synchronization Transformer" >}}

### Writer 2

Updates records in the source table

```sql
update TBL_SOURCE
SET UPDATE_FLAG = 'Y'
where PRIMARY_KEY=?
```

{{< image class="mx-auto d-block"  src="/images/knowledgebase/synchronization1-writer2-8.png" title="Synchronization Writer" >}}

[Data Synchronization Part 2]({{<ref "data-synchronization-part-2" >}})

{{< aetl >}}
