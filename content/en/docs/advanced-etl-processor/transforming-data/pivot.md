---
author: Peter Jonson
title: Working with Pivot
description: The Pivot transformation turns several rows of data into one; it makes a normalized data set into a less normalized but more compact version by pivoting the input data on a column value.
draft: false
tags: ['Transformation', 'Pivot']
date: 2022-09-17
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

The Pivot transformation turns several rows of data into one; it makes a normalized data set into a less normalized but more compact version by pivoting the input data on a column value. For example, a normalized sales report includes shop name, month and sales amount usually has several rows for any shop, with each row for that shop showing sales amount for a different month. By pivoting the data on the month column, the Pivot transformation object can output a data with a single row per shop. That single row lists all sales by the shop, with month names shown as column names, and sales amount shown as a value in the month column.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot.png" title="Pivot" >}}

## UnPivoted Data

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-source-data-example.png" title="UnPivoted Data*" >}}

## Pivoted Data

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivoted-data.png" title="Pivoted Data" >}}

Since there are more than one field to pivot let’s join Profit and Sales fields together first using tab a delimiter than pivot the data and split it again

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-data-flow.png" title="Pivoted Data" >}}

## Joining Data

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-joining-data.png" title="Joining Data" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-properties.png" title="Joining Data" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-keys.png" title="Joining Data Pivot Keys" >}}

## Data after Pivoting

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-data-after-pivoting.png" title="Data after Pivoting" >}}

## Splitting Pivoted Data

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-splitting-data.png" title="Splitting Pivoted Data" >}}

## Working with very wide Pivots

Quite ofter it is much easier to prepare pivot mapping in excel and paste it. Here is now:

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-excel-source.png" title="Working with very wide Pivots" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-paste.png" title="Working with very wide Pivots" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/pivot-paste-result.png" title="Working with very wide Pivots" >}}

{{< aetl >}}
