---
author: Peter Jonson
title: Loading data from the Cross/Pivot table
description: How to load data from the Cross/Pivot table
draft: false
tags: ['Import', 'Pivot']
date: 2015-06-14
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 3
---

Let us say we have table like the following in the database:

{{< table "table-striped table-bordered" >}}

| No  | Field      | Data Type |
| --- | ---------- | --------- |
| 1   | CUSTOMERID | CHAR      |
| 2   | YEAR       | DECIMAL   |
| 3   | MONTH      | DECIMAL   |
| 4   | PRODUCTID  | DECIMAL   |
| 5   | AMOUNT     | DECIMAL   |

{{< /table >}}

And a text files like the one below:

```
Year
CustomerID
ProductID
Month_1
Qty_1
…\
Month_12
Qty_12
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/main3.png" title="Pivot" >}}\
Click Data Source Button and check ‘Source file is a Pivot table’ check box and set First Field to 4, Blocks to 12 and Block length to 2\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/howto/pivot.png" title="Pivot" >}}

Finally we are ready to import data

Click to load data into the database {{< image src="/images/etl/advanced-etl-processor/import/run-button.png" title="Run Button" >}}

{{< aetl >}}
