---
author: Peter Jonson
title: Encode XML String
description: Encode XML String transformation function replaces characters
draft: false
tags: ['Transformation', 'Transformation Functions', 'Encode', 'XML']
date: 2022-09-17

group: advanced-etl-processor-enterprise-xml-html-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/encode_xml_string_function.png" title="Encode XML String transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                   |
| ----------- | ----------------------- |
| Category    | Transformation Function |
| Description | Replaces characters     |
| Properties  | None                    |

{{< /table >}}

- < => &lt;
- > => &qt;
- & => &amp;
- ' => &apos;
- " => &quot;

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
