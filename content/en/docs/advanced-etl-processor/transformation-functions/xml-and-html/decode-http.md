---
author: Peter Jonson
title: Decode HTTP
description: Decode HTTP transformation function decodes the escape characters (+ and %) in a string that comes from an HTTP message header
draft: false
tags: ['Transformation', 'Transformation Functions', 'Decode', 'Http']
date: 2022-09-17

group: advanced-etl-processor-enterprise-xml-html-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/decode_http_transformation_function.png" title="Decode HTTP transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                                                                                                                                                                                                                                                                                                                |
| Description | Decode HTTP decodes the escape characters (+ and %) in a string that comes from an HTTP message header. Plus characters (+) are converted into spaces. Percent signs (%) indicate that the next two characters are the hex representation of a character. If a percent sign is followed by another percent sign (%%), it is converted into a single percent sign. For example, the string %%+%3f is converted into % ? |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
