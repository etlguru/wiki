---
author: Peter Jonson
title: If Alpha
description: If Alpha transformation function checks if the data contains only Alpha characters
draft: false
tags: ['Transformation', 'Transformation Functions', 'Strings']
date: 2022-09-17

group: advanced-etl-processor-enterprise-strings-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_alpha_data_transformation_function.png" title="If Alpha transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                              |
| ----------- | -------------------------------------------------- |
| Category    | Transformation Function                            |
| Description | Checks if the data contains only Alpha characters. |
| Properties  | None                                               |
| Pass        | FCD,mmm,ABC                                        |
| Fail        | adc1,ad b,12 D                                     |

{{< /table >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
