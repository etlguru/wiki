---
author: Peter Jonson
title: Is UNC
description: Validation of UNC
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_unc_validation_function.png" title="Is UNC Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value               |
| ----------- | ------------------- |
| Category    | Validation Function |
| Description | Validation of UNC   |
| Properties  | Default             |
| Pass        | \\\\server\c$       |
| Fail        | ////server          |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
