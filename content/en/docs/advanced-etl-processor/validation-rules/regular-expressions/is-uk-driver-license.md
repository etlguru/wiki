---
author: Peter Jonson
title: Is UK Driver License
description: Validates the United Kingdom Drivers License format as described by the DVLA
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_uk_driver_licence_validation_function.png" title="Is UK Driver License Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                        |
| ----------- | ---------------------------------------------------------------------------- |
| Category    | Validation Function                                                          |
| Description | Validates the United Kingdom Drivers License format as described by the DVLA |
| Properties  | Default                                                                      |
| Pass        | JOHNS711215GG9SY                                                             |
| Fail        | JOHNS731215GG9SY                                                             |

{{< /table >}}

https://www.govtalk.gov.uk/gdsc/html/frames/default.htm.

**Matches:**

- Must be 16 characters
- First 5 characters are alphanumeric.
- Next 6 characters must be numeric
- Next 3 characters are alphanumeric
- Last 2 characters are alpha
- Second character of numeric section can only be 0
- Fourth and fifth characters of numeric section must be in the range 01 to 31

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
