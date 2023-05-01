---
author: Peter Jonson
title: Working with UnPivot
description: The UnPivot data transformation converts columns to rows.
draft: false
tags: ['Transformation', 'UnPivot']
date: 2022-06-05
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

The UnPivot data transformation converts columns to rows. It takes an unnormalized dataset and turns it into a normalized version by expanding values from multiple columns in a single record into multiple records with the same values in a single column.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot.png" title="Configuring the UnPivot Transformation" >}}

## Pivot types

There are two different kinds of Pivot tables:

### Multiple columns Pivot

For example, a dataset that lists shops' sales has one row for each shop, with the month and the sales amount shown in columns in the row.

The following diagram shows a data pivot with multiple columns:

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-multiple-column-pivot.png" title="Multiple columns Pivot" >}}

### Single column Pivot

For example, a file that holds a list of products bought by the customer with product codes delimited by semicolon.

The following picture shows a data pivot with a single pivot column.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-single-column-pivot.png" title="Single column Pivot" >}}

After the Unpivot transformation normalizes the data set, the data set contains a different row for each product that the customer purchased.

The following diagram shows a data after it has been unpivoted:

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-unpivoted-data.png" title="Single column Pivot" >}}

#### Pivoted Data Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-data-example.png" title="Pivoted Data Example" >}}

#### UnPivoted Data

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-group.png" title="UnPivoted Data" >}}

## Configuring the UnPivot Transformation

To change UnPivot properties double click on the object.

Fill in Description and select appropriate Pivot type

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-single-field.png" title="Configuring the UnPivot Transformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-multiple-fields.png" title="Configuring the UnPivot Transformation" >}}

**Note:**

Following actions apply only to multiple fields Pivot

Create all necessary Groups and Outputs

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-groups-out-1.png" title="Create all necessary Groups and Outputs" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-groups-out-2.png" title="Create all necessary Groups and Outputs" >}}

Once it is done Map Input fields to Outputs and Groups

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-map-input-fields-9.png" title=" Map Input fields to Outputs and Groups" >}}

## Result

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/unpivot-result.png" title="Result" >}}

{{< aetl >}}
