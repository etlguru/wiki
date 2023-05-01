---
author: Peter Jonson
title: Date Format
description: Date Format transformation function returns Date in yyyy-mm-dd hh:nn:ss.fff format
draft: false
tags: ['Transformation', 'Transformation Functions', 'Date']
date: 2022-03-02

group: advanced-etl-processor-enterprise-date-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

In order to load data into Date/Time fields, it should be converted into 'yyyy-mm-dd hh:nn:ss.fff' format

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/date_format_transformation_function.png" title="Date Format" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                             |
| ----------- | ------------------------------------------------- |
| Category    | Transformation Function                           |
| Description | Returns Date in ‘yyyy-mm-dd hh:nn:ss.fff' format. |
| Properties  |                                                   |

{{< /table >}}

- It is possible to apply multiple data formats
- The first format which works is used
- if the data is already in YYYY-MM-DD HH:NN:SS.FFF format there is no need to convert it

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/date_format_data_transformation_function_properties.png" title="Date Format Properties" >}}
\
{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
