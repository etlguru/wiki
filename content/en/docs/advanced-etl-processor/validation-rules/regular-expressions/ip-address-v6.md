---
author: Peter Jonson
title: Is IP Address V6
description: Validates all IPv6 text representations as defined within RFC 2373
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_ip_address_v6_validation_function.png" title="Is IP Address V6 Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                              |
| ----------- | ------------------------------------------------------------------ |
| Category    | Validation Function                                                |
| Description | Validates all IPv6 text representations as defined within RFC 2373 |
| Properties  | Default                                                            |
| Pass        | ::0:0:0:FFFF:129.144.52.38                                         |
| Fail        | FEDC:BA98:7654:3210:FEDC:BA98:7654:3210:1234                       |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
