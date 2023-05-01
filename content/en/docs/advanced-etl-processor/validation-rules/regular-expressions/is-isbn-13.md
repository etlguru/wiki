---
author: Peter Jonson
title: Is ISBN 13
description: Validation of new 13 digits ISBN.
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_isbn_13_validation_function.png" title="Is ISBN 13 Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                |
| ----------- | ---------------------------------------------------------------------------------------------------- |
| Category    | Validation Function                                                                                  |
| Description | Validation of new 13 digits ISBN. The ISBN number must be preceded by the text "ISBN:" or "ISBN-13:" |
| Properties  | Default                                                                                              |
| Pass        | ISBN-13: 978-0-5960-0289-3                                                                           |
| Fail        | ISBN-10: 0596002890                                                                                  |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
