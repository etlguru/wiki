---
author: Maria Salter
title: Blob Field is empty
description: This Article describes how to fix problems with reading data from Blob fields
draft: false
tags: ['Knowledgebase', 'Blob']
date: 2022-04-13
group: knowledgebase-issues
layout: docs
---

When loading data from ODBC/ACCESS/SQL Server source it is possible to have all blob fields blank.

The problem can be easily addressed by rewriting SQL and making all blob fields last in the query

**Change**

```sql
select field1,blob1,field2 from table
```

**to**

```sql
select field1,field2, blob1 from table
```

**Also Read:**

[Invalid Descriptor Index]({{<ref "invalid-descriptor-index" >}})

{{< aetl >}}
