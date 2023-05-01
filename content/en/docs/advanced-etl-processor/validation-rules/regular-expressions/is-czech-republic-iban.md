---
author: Peter Jonson
title: Is Czech Republic IBAN
description: Validates Czech International Bank Account Number
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23

group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_czech_republic_iban_validation_function.png" title="Is Czech Republic IBAN Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                             |
| ----------- | ------------------------------------------------- |
| Category    | Validation Function                               |
| Description | Validates Czech International Bank Account Number |
| Properties  | Default                                           |
| Pass        | CZ65 0800 0000 1920 0014 5399                     |
| Fail        | CZ65-0800-0000-1920-0014-5399                     |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
