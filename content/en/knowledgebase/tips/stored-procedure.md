---
author: Maria Salter
title: Using Stored Procedures to load data
description: Using stored procedure to perform complex ETL processes
draft: false
tags: ['Knowledgebase', 'Stored procedure']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

Here is an example of how to load data using a stored procedure.

Using this approach gives the user the ability to perform complex transformations inside the database, for example, the user may have a look table that is just too big to pull out or a user may want to reuse existing code.

{{< alert color="secondary" >}}Please note that bulk loading is always faster{{< /alert >}}

## Table Creation Script

```sql
CREATE TABLE [dbo].[orders](
[customerid] [char](5) NOT NULL,
[orderno] [decimal](20, 5) NOT NULL,
[orderdate] [smalldatetime] NOT NULL,
[amount] [decimal](16, 2) NOT NULL
) ON [PRIMARY]
```

## Stored Procedure Script

```sql
CREATE PROCEDURE [dbo].[p-Populate-Data]
(
@customerid char(5),
@orderno decimal(20,5),
@orderdate smalldatetime,
@amount decimal(16, 2)
)
AS
begin
set nocount on
insert into orders (customerid,orderno,orderdate,amount)
values(@customerid,@orderno,@orderdate,@amount)
end
```

## Transformation

{{< image class="mx-auto d-block"  src="/images/knowledgebase/stored-procedure-1.png" title="Stored procedure" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/stored-procedure-2.png" title="Stored procedure" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/stored-procedure-3.png" title="Stored procedure" >}}
\
{{< alert color="secondary" >}}Both Visual Importer ETL and Advanced ETL Processor support working with stored procedures{{< /alert >}}

{{< aetl >}}
