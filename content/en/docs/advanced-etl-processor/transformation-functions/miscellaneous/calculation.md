---
author: Peter Jonson
title: Calculation
description: Calculation transformation function provides a flexible way of transforming the data. The programming language used is very close to Pascal. It is also possible to use Python as scripting language
draft: false
tags: ['Transformation', 'Transformation Functions', 'Miscellaneous', 'Script', 'Pascal', 'Python']
date: 2022-09-17

group: advanced-etl-processor-enterprise-miscellaneous-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/calcualtion_transformation_function.png" title="Calculation transformation" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                                  |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                                                                |
| Description | Allows the end user to write scripts to transform data. The programming language used is very close to Pascal. It is also possible to use Python as scripting language |

{{< /table >}}

- All data is coming in into the calculation as strings
- The data is coming out of the calculation as a string.
- All nulls are replaced with empty strings.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/calculation_properties_2.png" title="Calculation transformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/calcualtion_properties.png" title="Calculation transformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/calcualtion_properties2.png" title="Calculation transformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/expressions_builder.png" title="Calculation transformation" >}}
\
{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

## Useful Links

- [Scripting Language]({{<relref "docs/advanced-etl-processor/scripting-language" >}})
- [Supported Functions List]({{<ref "supported-functions-list" >}})
- [Best Practice for Calculations]({{<relref "/knowledgebase/tips/best-practice-for-calculations" >}})
- [Working with python]({{<ref "working-with-python" >}})
- [Download Python](https://www.python.org/downloads)

{{< alert color="warning">}}Calculation transformation is the slowest way to transform the data and it should be avoided.
If you do not know how to transform the data ask the question on our support forum and we will help you.
{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
