---
author: Peter Jonson
title: Generating Primary Keys and Defaults
description: Generating Primary Keys and Defaults
draft: false
tags: ['Writer']
date: 2023-01-05
group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/sql-function.png" title="PostgreSql Writer" >}}

**When field is not mapped to anything:**

Enter value (New York for example) into SQL function field and
following SQL would be executed while inserting the data.

```sql
insert into Customers (Customer,,,,City)
values (CustomerValue,,,"New-York")
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/default.png" title="Writer Default" >}}

**When field is mapped:**

Enter value (New York for example) into default field and
this value will be used for inserts if source field is null or empty.

**Note:**

To insert empty string enter ’’ into default field.

{{< aetl >}}
