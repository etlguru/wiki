---
author: Peter Jonson
title: Lookup
description: Lookup transformation function substitutes values using mapping table. The mapping table can be populated manually or loaded from file/database
draft: false
tags: ['Transformation', 'Transformation Functions', 'Lookup']
date: 2022-08-01

group: advanced-etl-processor-enterprise-lookup-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_transformation_function.png" title="Range Lookup transformation function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                           |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                         |
| Description | This function substitutes values using mapping table. The mapping table can be populated manually or loaded from file/database. |
| Properties  |                                                                                                                                 |

{{< /table >}}

## Manually populating Mapping table

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_properties.png" title="Range Lookup transformation function" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_properties_1.png" title="Range Lookup transformation function" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_properties_2.png" title="Range Lookup transformation function" >}}

## Populating Mapping table using database/file

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_properties_11.png" title="Range Lookup transformation function" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_properties_12.png" title="Range Lookup transformation function" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_properties_13.png" title="Range Lookup transformation function" >}}
\
{{< alert color="secondary">}}Once the file format is defined it is important to define the mapping for input and output fields.{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/lookup_properties_mapping.png" title="Range Lookup transformation function" >}}
\
{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

## Video Tutorial

{{< youtube id="pYE1YZn9eaM" class="ratio ratio-16x9" >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
