---
author: Peter Jonson
title: Encode HTTP
description: Encode HTTP transformation function converts all characters in the AStr parameter except for the letters A through Z
draft: false
tags: ['Transformation', 'Transformation Functions', 'Encode', 'Http']
date: 2022-09-17

group: advanced-etl-processor-enterprise-xml-html-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/encode_http_transformation_function.png" title="Encode HTTP transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Description | Encode HTTP converts all characters in the AStr parameter except for the letters A through Z (and a through z), numerals 0 through 9, the asterisk (\*), dollar sign ($), exclamation point (!), at sign (@), period (.), underscore (\_), single quote ('), comma (,) parentheses, and hyphen (-). Spaces are converted to plus characters (+), and all other characters are converted into hex values preceded by the percent sign (%). For example, the string % ? is converted into %%+%3f |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
