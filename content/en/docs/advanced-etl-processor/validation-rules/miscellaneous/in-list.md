---
author: Peter Jonson
title: In List
description: Checks if the data exists within supplied list
draft: false
tags: ['Transformation', 'Validation Rules', 'Miscellaneous']
date: 2023-02-23
group: advanced-etl-processor-enterprise-miscellaneous-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/in_list_validation_function.png" title="In List" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                                                |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Category    | Validation Function                                                                                                                                                                  |
| Description | Checks if the data exists within supplied list values                                                                                                                                |
| Properties  | List of values can be entered by the user or extracted from the file(s) or database. When source data for the “List of values” consists of more than 1 field only first one is used. |

{{< /table >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/in_list_properties.png" title="In List" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_in_list_properties.png" title="In List" >}}
\
{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
