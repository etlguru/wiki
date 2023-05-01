---
author: Peter Jonson
title: Is Canadian Branch-Transit/Bank code
description: Validates Canadian Branch-Transit number. The branch number must be 3 or 4 digits then '-' then five digits
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23

group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_canadian_barnch-transit_validation_function_.png" title="Is Canadian Branch-Transit/Bank code Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                       |
| ----------- | ----------------------------------------------------------------------------------------------------------- |
| Category    | Validation Function                                                                                         |
| Description | Validates Canadian Branch-Transit number. The branch number must be 3 or 4 digits then '-' then five digits |
| Properties  | Default                                                                                                     |
| Pass        | 654-45654                                                                                                   |
| Fail        | 455645564                                                                                                   |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
