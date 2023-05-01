---
author: Peter Jonson
title: Decode Base 64
description: Decode Base 64 transformation function performs Base 64 Decoding
draft: false
tags: ['Transformation', 'Transformation Functions', 'Decode']
date: 2022-09-17

group: advanced-etl-processor-enterprise-xml-html-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/encode_base_64_transformation_function.png" title="Decode Base 64 transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                      |
| ----------- | -------------------------- |
| Category    | Transformation Function    |
| Description | Performs Base 64 Decoding. |
| Properties  | None                       |

{{< /table >}}

Base64 is a group of similar encoding schemes that represent binary data in an ASCII string format by translating it into a radix-64 representation. The Base64 term originates from a specific MIME content transfer encoding.

Base64 encoding schemes are commonly used when there is a need to encode binary data that needs be stored and transferred over media that are designed to deal with textual data. This is to ensure that the data remains intact without modification during transport. Base64 is commonly used in a number of applications including email via MIME, and storing complex data in XML.

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
