---
author: Peter Jonson
title: Updating or Deleting Records
description: How to Update/Delete records
draft: false
tags: ['Import']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 4
---

In order to Update/Delete, records user must specify an update key.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/update-key.png" title="Updating or Deleting Records" >}}

For the example provided below, the following SQL is executed

(Update key is CustomerId, OrderNo)

## Add New Records

```sql
Select count(*)
from [DEMO].[dbo].[orders]
where CustomerId=? And OrderNo=?
```

If no records found then new records are added

## Add New And Update Old Records

```sql
Select count(*)
from [DEMO].[dbo].[orders]
where CustomerId=? And OrderNo=?
```

If any records found they are updated

```sql
Update [DEMO].[dbo].[orders]
set orderdate=?,
amount=?
where customerid=? And OrderNo=?
```

If no records found then new records are added

## Update Records

```sql
Update [DEMO].[dbo].[orders]
set OrderDate=?,
Amount=?
where CustomerId=? And OrderNo=?
```

## Delete Records

```sql
Delete from [DEMO].[dbo].[orders]
Where CustomerId=? And OrderNo=?
```

It is also possible to manually edit Insert/Update/Delete/Count SQL Statements.
Tick user-defined SQL than edit every SQL statement individually.
To regenerate the SQL statements clear it and open it again

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/update-records1.png" title="User definable sql" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/update-records2.png" title="User definable sql" >}}

{{< aetl >}}
