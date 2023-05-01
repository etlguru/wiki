---
author: Maria Salter
title: Executing single copy of the package
description: This article describes how to execute single copy of the package
draft: false
tags: ['Knowledgebase', 'Package']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## The Problem

Quite often it is necessary to make sure that only one copy of the package is being executed at a given time
For example, the package below is being executed every 2 minutes but it might take more than 2 minutes to complete
The package is creating text files it is not possible to open the same file twice for writing.
So we have to check if the same package is being executed and if not abort the execution

{{< image class="mx-auto d-block"  src="/images/knowledgebase/check-object-execution1-1.png" title="Check Object Execution" >}}

## The Solution

This can be easily done by using SQL Data Check Action

### Example

SQL Data Check uses SQL scripts to check data in the database.
For example, the user may write the following SQL:

```sql
Select count(*) from table
```

Execution will be successful if the value of the first field of lookup query is more than 0
Execution will fail if the value of the first field of lookup query is
equals to 0 or less than 0 or the field type is not numeric.

Using the same approach we can query QUEUE and QUEUE_ACTIONS tables

```sql
Select Count(*) as RC from
( select OBJECT_ID from QUEUE WHERE STATUS='R' and OBJECT_ID=3924
union all
select OBJECT_ID from QUEUE_ACTIONS WHERE STATUS='R' and OBJECT_ID=3924
)
```

{{< image class="mx-auto d-block"  src="/images/knowledgebase/check-object-execution3-2.png" title="Check Object Execution" >}}
\
{{< alert color="secondary" >}}3924 is a package ID{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/check-object-execution2-3.png" title="Check Object Execution" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/check-object-execution4-4.png" title="Check Object Execution" >}}
\
{{< alert color="secondary" >}}Status=R means running.{{< /alert >}}

- [Repository Tables]({{<ref "repository-tables" >}})

{{< aetl >}}
