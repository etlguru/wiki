---
author: Maria Salter
title: Best Practice for Calculations
description: This Article describes best practices for ETL calculations
draft: false
tags: ['Knowledgebase', 'Calculation', 'Script']
date: 2022-09-17
group: knowledgebase-issues
layout: docs
---

Let us consider calculating profit as example

```
Profit := Income-Expenditure;
```

There is no guarantee that Income and Expenditure data will always have a numeric data type.
Some users may prefer to use 'No Income' or 'No Expenditure' values

The best way to avoid problems with data quality is to follow the pattern below.

- Create variables for every input parameter.
- Assign input parameters to variables inside try expect block
- Perform calculations
- Return value

**Example:**

```
Var
vIncome: Float;
vExpenditure: Float;

begin
// Converting strings to Floats
Try
vIncome:=Income;
except
vIncome:=0;
end;

try
vExpenditure:=Expenditure;
except
vExpenditure:=0;
end;

// Calculation

Result := vIncome-vExpenditure;
end;

```

## Useful Links

- [Scripting Language]({{<relref "docs/advanced-etl-processor/scripting-language" >}})
- [Supported Functions List]({{<ref "supported-functions-list" >}})
- [Working with python]({{<ref "working-with-python" >}})
- [Download Python](https://www.python.org/downloads)

{{< aetl >}}
