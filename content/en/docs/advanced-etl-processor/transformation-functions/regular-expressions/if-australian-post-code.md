---
author: Peter Jonson
title: If Australian Post Code
description: Australian postal code verification. Australia has 4-digit numeric postal codes with the following state based specific ranges
draft: false
tags: ['Transformation', 'Transformation Functions', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_australian_post_code_tranformation_finction.png" title="If Australian Post Code" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                                        |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                                                                      |
| Description | Australian postal code verification. Australia has 4-digit numeric postal codes with the following state based specific ranges. ACT: 0200-0299 and 2600-2639. NSW: 1000-1999 |
| Properties  | Default                                                                                                                                                                      |
| Pass        | 0200                                                                                                                                                                         |
| Fail        | 0300                                                                                                                                                                         |
|             |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
