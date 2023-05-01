---
author: Peter Jonson
title: Running Total
description: The running total represents an instantaneous total of all the "quantities" of stuff that can be reviewed at any time during the recording period to determine what the total was at that time of review
draft: false
tags: ['Transformation', 'Transformation Functions', 'Miscellaneous']
date: 2022-09-17

group: advanced-etl-processor-enterprise-miscellaneous-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/running_totals_transformation_function.png" title="Running total" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                                                                     |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                                                                                                   |
| Description | The running total represents an instantaneous total of all the "quantities" of stuff that can be reviewed at any time during the recording period to determine what the total was at that time of review. |

{{< /table >}}

Here's a sample of a running total of that store's receipts:

{{< table "table-striped table-bordered" >}}

| Transaction           | Value                 |
| --------------------- | --------------------- |
| Sale 1: $6.49         | Running total: $6.49  |
| Sale 2: $2.81         | Running total: $9.30  |
| Sale 3: $1.37         | Running total: $10.67 |
| Sale 4: Refund: $0.89 | Running total: $9.78  |
| Sale 5: $5.26         | Running total: $15.04 |

{{< /table >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/running_totals_transformation_function_properties.png" title="Running total properties" >}}
\
{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
