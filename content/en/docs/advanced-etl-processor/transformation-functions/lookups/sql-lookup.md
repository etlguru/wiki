---
author: Peter Jonson
title: SQL Lookup
description: SQL Lookup transformation function retrieves values from the database using SQL. Parameters are replaced with actual values before the execution
draft: false
tags: ['Transformation', 'Transformation Functions', 'Lookup']
date: 2022-08-01
group: advanced-etl-processor-enterprise-lookup-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/sql_lookup_transformation_function.png" title="SQL Lookup transformation function" >}}

SQL Lookup is the slowest transformation. It is used only when nothing else is working.

{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                        |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                      |
| Description | This function retrieves values from the database using SQL. Parameters are replaced with actual values before the execution. |
| Properties  |                                                                                                                              |

{{< /table >}}

## Parameters

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/sql_lookup_transformation_function_page1.png" title="SQL Lookup transformation function" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/sql_lookup_transformation_function_page2.png" title="SQL Lookup transformation function" >}}
\
**Note:** \<Parameter1> inside SQL box

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/sql_lookup_transformation_function_page3.png" title="SQL Lookup transformation function" >}}
\
**Note:** single quotes around '\<Parameter1>', use this approach for string parameters

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/sql_lookup_transformation_function_page4.png" title="SQL Lookup transformation function" >}}
\
{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

## Video Tutorial

{{< youtube id="pYE1YZn9eaM" class="ratio ratio-16x9" >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
