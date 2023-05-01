---
author: Peter Jonson
title: If Irish VAT Number
description: Irish VAT Numbers format verification with support for optional member state definition
draft: false
tags: ['Transformation', 'Transformation Functions', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_irish_vat_number_tranformation_finction.png" title="If Irish VAT Number" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                    |
| ----------- | ---------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                  |
| Description | Irish VAT Numbers format verification with support for optional member state definition. |
| Properties  | Default                                                                                  |
| Pass        | IE4\*12345Z                                                                              |
| Fail        | IE4-12345Z                                                                               |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
