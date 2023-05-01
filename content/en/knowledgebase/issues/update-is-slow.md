---
author: Maria Salter
title: Update is slow
description: Update is slow
draft: false
tags: ['Knowledgebase', 'Transformation', 'Performance']
date: 2023-03-14
group: knowledgebase-issues
layout: docs
---

Number of customers complained to us that all operations except Add all records are slow and even worse some of them believe that it is the limitation of our software

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/add-delete-transformation.png" title="Add/Delete Transformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/update-key.png" title="Update key" >}}

Note: In order to Update/Delete records update key must be provided.

## Add New And Update Old Records

Our Update key is CustomerId and OrderNo

Let think about how it works

The first step we need to figure out if the record exists in the database so we run count

```sql
Select count(*)
from [orders]
where CustomerId=? and OrderNo=?
```

If any records found [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) will update them by executing

```sql
Update [orders]
set orderdate=?,
amount=?
where customerid=? And OrderNo=?
```

If no records found Advanced ETL inserts data into the order table

Insert is very quick because it does not do anything with existing records.\
The count is slower because in order to find the record full scan of the table must be performed (or index scan if present)\
The update is even slower be because it scans the table and updates the data

Now imagine that our source data has 10,000 records

For every record, we must execute two SQL statements:

count and insert
or
count and update

So we run 20,000 SQL statements in total.\
Every statement takes time to execute.

The more records there is in the target table the more time it takes to execute.

Bear in mind that it is not our software that executes statements it is the database it is connected to.

## Large tables

This works very well for small tables but what if we have millions of records?
In this case, we recommend using a temporary table.

All data gets loaded into a temporary table (orders_tmp).

And then update and insert SQL statements are executed:

```sql
Update orders
set orderdate = orders_tmp.orderdate,
amount = orders_tmp.amount
from orders_tmp
where orders.customerid = orders_tmp.customerid And
orders.OrderNo = orders_tmp.OrderNo

insert into orders (customerid,OrderNo,orderdate,amount)
select customerid,OrderNo,orderdate,amount
FROM orders_tmp e
where not exists (
select \*
from orders
orders.customerid = e.customerid And
orders.OrderNo = e.OrderNo)
```

{{< image class="mx-auto d-block"  src="/images/knowledgebase/sql-after-1.png" title="SQL After" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/sql-after-2.png" title="SQL After" >}}

You might need to use different syntax for the database you work with

{{< aetl >}}
