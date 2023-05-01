---
author: Maria Salter
title: Making ETL Objects Read Only
description: This article explains how to make Objects read only
draft: false
tags: ['Knowledgebase', 'Transformation', 'Package']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

No one wants to be famous for the wrong reason, this is why it is important to prevent changes to ETL transformations once they are deployed to production.

This can be easily done with the latest versions of [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor//overview.html) and [Visual Importer ETL](https://www.etl-tools.com/visual-importer-etl-enterprise/overview.html)

All the user have to do is to press the read-only button.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/readonly-package.png" title="Readonly package" >}}
\
{{< alert color="secondary" >}}It is also possible to make several objects read-only by selecting the top node from the objects tree.{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/readonly-menu.png" title="Readonly Menu" >}}

## For Oracle

```sql
ALTER TABLE OBJECTS_TREE ADD READ_ONLY Integer NULL
```

## For MS SQL Server

```sql
ALTER TABLE OBJECTS_TREE ADD READ_ONLY decimal(28, 0) NULL
```

## For MySQL

```sql
ALTER TABLE OBJECTS_TREE ADD READ_ONLY Numeric
```

## For PostgreSQL

```sql
ALTER TABLE OBJECTS_TREE ADD read_only double-precision null
```

## For Interbase

```sql
ALTER TABLE OBJECTS_TREE ADD READ_ONLY DOUBLE PRECISION NOT NULL
```

We would like to thank Orlando Cabrera from Xerox Canada Ltd for providing us with valuable feedback

{{< aetl >}}
