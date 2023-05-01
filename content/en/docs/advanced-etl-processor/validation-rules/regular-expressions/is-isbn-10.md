---
author: Peter Jonson
title: Is ISBN 10
description: Validation of 10 digits ISBN.
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_isbn_10_validation_function.png" title="Is ISBN 10 Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                            |
| ----------- | ------------------------------------------------------------------------------------------------ |
| Category    | Validation Function                                                                              |
| Description | Validation of 10 digits ISBN. The ISBN number must be preceded by the text "ISBN:" or "ISBN-10:" |
| Properties  | Default                                                                                          |
| Pass        | ISBN-10: 0-93028-923-4                                                                           |
| Fail        | ISBN-13: 978-0-5960-0289-3                                                                       |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
