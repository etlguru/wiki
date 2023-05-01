---
author: Peter Jonson
title: Is Irish VAT Number
description: Irish VAT Numbers format verification with support for optional member state definition.
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_irish_vat_number_validation_function.png" title="Is Irish VAT Number Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                    |
| ----------- | ---------------------------------------------------------------------------------------- |
| Category    | Validation Function                                                                      |
| Description | Irish VAT Numbers format verification with support for optional member state definition. |
| Properties  | Default                                                                                  |
| Pass        | IE4\*12345Z                                                                              |
| Fail        | IE4-12345Z                                                                               |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
