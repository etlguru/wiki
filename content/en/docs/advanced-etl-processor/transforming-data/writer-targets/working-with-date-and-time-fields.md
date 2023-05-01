---
author: Peter Jonson
title: Working with Date/Time fields
description: Working with Date/Time fields
draft: false
tags: ['Writer', 'Date', 'Time']
date: 2022-09-17

group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

In order to load data into target database's Date or time fields, it should be converted into 'YYYY-MM-DD HH:NN:SS.FFF' format. This transformation is done by "Date format" transformation function.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/date_format_transformation_function.png" title="Date Format Transformation Function" >}}

- It is possible to apply multiple date formats.
- The first format which works is used.
- if the data is already in YYYY-MM-DD HH:NN:SS.FFF format, there is no need to convert it.
- Be aware of leading and trailing spaces
- When data is loaded into time field date part is ignored

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/date_format_data_transformation_function_properties.png" title="Date Format Data Transformation Function properties" >}}

{{< aetl >}}
