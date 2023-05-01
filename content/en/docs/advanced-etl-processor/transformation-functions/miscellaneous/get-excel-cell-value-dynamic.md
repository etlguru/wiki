---
author: Peter Jonson
title: Get Excel Cell Value Dynamic
description: Get Excel Cell Value Dynamic transformation function extracts sigle cell value from an excel file
draft: false
tags: ['Transformation', 'Transformation Functions', 'Miscellaneous', 'Excel']
date: 2023-03-05

group: advanced-etl-processor-enterprise-miscellaneous-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/get_excel_cell_value_dynamic_transformation_function.png" title="Get Excel Cell Value Dynamic transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                  |
| ----------- | -------------------------------------- |
| Category    | Transformation Function                |
| Description | Extracts Cell value from an excel file |
| Properties  |                                        |

{{< /table >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/get_excel_cell_value_dynamic_transformation_function_properties.png" title="Get Excel Cell Value Dynamic transformation function" >}}
\
{{< alert color="secondary">}}In most cases, "Cache values" must be checked. When "Cache values" is checked function opens and closes the Excel file for every source record, It takes time to open the file and get the cell value.{{< /alert >}}

Here is another way of reading excel cell:\
[How to read a single excel cell value](https://www.etl-tools.com/automation/0004-how-to-read-a-single-excel-cell-value.html)

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
