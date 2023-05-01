---
author: Peter Jonson
title: Accumulate Strings
description: Accumulate Strings transformation function concatenates value with previous value
draft: false
tags: ['Transformation', 'Transformation Functions', 'Miscellaneous']
date: 2022-09-17

group: advanced-etl-processor-enterprise-miscellaneous-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/accumulate_strings_transformation_function.png" title="Accumulate Strings" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                   |
| ----------- | --------------------------------------- |
| Category    | Transformation Function                 |
| Description | Concatenates value with previous value. |

{{< /table >}}

## Usage example

### Source Data

{{< table "table-striped table-bordered" >}}

| Record Number | Key | Value |
| ------------- | --- | ----- |
| 1             | 1   | V1    |
| 2             | 1   | V2    |
| 3             | 2   | V3    |
| 4             | 2   | V4    |
| 5             | 2   | V5    |
| 6             | 2   | V6    |

{{< /table >}}

### Result

{{< table "table-striped table-bordered" >}}

| Record Number | Key | Value    |
| ------------- | --- | -------- |
| 1             | 1   | V1       |
| 2             | 1   | V1V2     |
| 3             | 2   | V3       |
| 4             | 2   | V3V4     |
| 5             | 2   | V3V4V5   |
| 6             | 2   | V3V4V5V6 |

{{< /table >}}
\

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
