---
author: Peter Jonson
title: Is Estonian VAT Number
description: Estonian VAT Numbers format verification with support for optional member state definition.
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23

group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_estonian_vat_number_validation_function.png" title="Is Estonian VAT Number Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                       |
| ----------- | ------------------------------------------------------------------------------------------- |
| Category    | Validation Function                                                                         |
| Description | Estonian VAT Numbers format verification with support for optional member state definition. |
| Properties  | Default                                                                                     |
| Pass        | EE123456789                                                                                 |
| Fail        | EE12345678                                                                                  |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
