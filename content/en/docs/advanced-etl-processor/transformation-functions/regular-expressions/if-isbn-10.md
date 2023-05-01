---
author: Peter Jonson
title: If ISBN 10
description: Validation of 10 digits ISBN
draft: false
tags: ['Transformation', 'Transformation Functions', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_isbn_10_tranformation_finction.png" title="If ISBN 10" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                            |
| ----------- | ------------------------------------------------------------------------------------------------ |
| Category    | Transformation Function                                                                          |
| Description | Validation of 10 digits ISBN. The ISBN number must be preceded by the text "ISBN:" or "ISBN-10:" |
| Properties  | Default                                                                                          |
| Pass        | ISBN-10: 0-93028-923-4                                                                           |
| Fail        | ISBN-13: 978-0-5960-0289-3                                                                       |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
