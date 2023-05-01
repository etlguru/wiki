---
author: Peter Jonson
title: If ISBN 13
description: Validation of new 13 digits ISBN
draft: false
tags: ['Transformation', 'Transformation Functions', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_isbn_13_tranformation_finction.png" title="If ISBN 13" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                |
| ----------- | ---------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                              |
| Description | Validation of new 13 digits ISBN. The ISBN number must be preceded by the text "ISBN:" or "ISBN-13:" |
| Properties  | Default                                                                                              |
| Pass        | ISBN-13: 978-0-5960-0289-3                                                                           |
| Fail        | ISBN-10: 0596002890                                                                                  |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
