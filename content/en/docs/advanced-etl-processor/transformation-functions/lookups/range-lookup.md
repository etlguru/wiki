---
author: Peter Jonson
title: Range Lookup
description: Range Lookup transformation function finds a key for a given range
draft: false
tags: ['Transformation', 'Transformation Functions', 'Lookup']
date: 2022-08-01
group: advanced-etl-processor-enterprise-lookup-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/range_lookup_transformation_function.png" title="Range Lookup transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                                                                                                                                                                                                     |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                                                                                                                                                                                                                                   |
| Description | Performing range lookups (or finding a key for a given range) is a common ETL operation in data warehousing scenarios. It's especially useful for historical loads and late arriving fact situations, where you're using type 2 dimensions and you need to locate the key which represents the dimension value for a given point in time. |
| Properties  |                                                                                                                                                                                                                                                                                                                                           |

{{< /table >}}

{{< alert color="secondary">}}Data for lookup can be entered manually or loaded from the database or a file.{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/range_lookup_transformation_function_properties.png" title="Range Lookup transformation function" >}}
\
{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

**Video Tutorial**

{{< youtube id="pYE1YZn9eaM" class="ratio ratio-16x9" >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
