---
author: Peter Jonson
title: Split RegX Dynamic
description: Splits string using regular expression
draft: false
tags: ['Transformation', 'Transformation Functions', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/split_regx_tranformation_dynamic_finction.png" title="Split RegX Dynamic" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                  |
| ----------- | -------------------------------------- |
| Category    | Transformation Function                |
| Description | Splits string using regular expression |
| Properties  | Parameter is regular expression        |

{{< /table >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/split_regx_tranformation_finction_properties.png" title="Split RegX Dynamic Properties" >}}

**Notes**

"Use groups" option enables advanced splitting functionality

For example in this regular expression (?<startfield>._)CTL._\_(?<datefield>[0-9]{8}).\*\.TXT startfield and datefield are two GROUPS.
These groups are used to split the string

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
