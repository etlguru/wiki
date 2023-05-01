---
author: Peter Jonson
title: SQL Data Check Action
description: The SQL Check Action object can be used to check data queries in the database, to ensure that data integrity and ensure that results are returned as expected.
draft: false
tags: ['Package', 'Action', 'SQL', 'Check']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

## About

The SQL Check Action object can be used to check data queries in the database, to ensure that data integrity and ensure that results are returned as expected.

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/sql-data-check-action.png" title="Workflow tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/check-sql-variables.png" title="After execution tab" >}}

## Example

SQL Data Check uses SQL scripts to check data in the database.

For example, the user may write the following SQL:

```sql
Select count(*) from table
```

- Execution is successful if the value of the first field of lookup query is more than 0
- Execution fails if the value of the first field of lookup query is equals to 0 or less than 0 or field type is not numeric.

{{< aetl >}}
