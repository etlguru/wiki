---
author: Peter Jonson
title: Update/Delete Records
description: How to Update/Delete Records
draft: false
tags: ['Writer', 'Update', 'Delete']
date: 2022-09-17

group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

In order to Update/Delete records you must specify update key.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/update-key.png" title="Update Key" >}}
\
For the example provided below, [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) will execute the following SQL

(Update key is CustomerId, OrderNo).

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/add-delete-transformation.png" title="Add/Delete Transformation" >}}

**Add New And Update Old Records**

```sql
Select count(*)
from [DEMO].[dbo].[orders]
where CustomerId=? And OrderNo=?
```

If any records found Advanced ETL will update them by executing

```sql
Update [DEMO].[dbo].[orders]
set orderdate=?,
amount=?
where customerid=? And OrderNo=?
```

If no records found Advanced ETL will add new records

**Update Records**

```sql
Update [DEMO].[dbo].[orders]
set OrderDate=?,
Amount=?
where CustomerId=? And OrderNo=?
```

**Delete Records**

```sql
Delete from [DEMO].[dbo].[orders]
Where CustomerId=? And OrderNo=?
```

{{< alert color="secondary">}}It is also possible to manually edit Insert/Update/Delete/Count SQL.\  
Tick user defined SQL than edit every SQL statement individually.\  
To regenerate the SQL statements clear it and open it again.{{< /alert >}}

{{< aetl >}}
