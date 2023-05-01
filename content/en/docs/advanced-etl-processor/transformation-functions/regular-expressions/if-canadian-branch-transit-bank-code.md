---
author: Peter Jonson
title: If Canadian Branch-Transit/ Bank code
description: Validates Canadian Branch-Transit number. The branch number must be 3 or 4 digits then '-' then five digits
draft: false
tags: ['Transformation', 'Transformation Functions', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_canadian_branch_transit_tranformation_finction.png" title="If Canadian Branch-Transit/ Bank code" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                       |
| ----------- | ----------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                     |
| Description | Validates Canadian Branch-Transit number. The branch number must be 3 or 4 digits then '-' then five digits |
| Properties  | Default                                                                                                     |
| Pass        | 654-45654                                                                                                   |
| Fail        | 455645564                                                                                                   |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
