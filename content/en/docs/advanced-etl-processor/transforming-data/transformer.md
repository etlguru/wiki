---
author: Peter Jonson
title: Working with Transformer
description: Working with Transformer
draft: false
tags: ['Transformation', 'Transformer']
date: 2022-08-01
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer.png" title="Transformer" >}}
\
{{< alert color="secondary">}}To change Transformer properties double click on it{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-properties.png" title="Transformer Properties" >}}
\
{{< alert color="secondary">}}If no data is present in the grid check the previous step execution log.{{< /alert >}}

**About input and output fields:**
*If a transformer is connected to any object other than the writer it is possible to modify the list of Outputs. When the transformer is connected to writer list of Outputs is taken from Writer.
*List of Input fields is taken from the previous object

## Transformer Toolbar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-toolbar.png" title="Transformer Toolbar" >}}

1. Properties
1. Create new tab
1. Cut
1. Copy
1. Paste
1. Delete
1. Redo
1. Undo
1. Align Left
1. Arrange Vertically
1. Align Right
1. Align Bottom
1. Arrange Horizontally
1. Align Top
1. Space Horizontally
1. Space Vertically
1. Snap to grid/show grid
1. Prints Mapping
1. Print Preview Mapping
1. Automap data
1. Delete All objects
1. Delete All Links
1. Search Objects
1. Process Data
1. First Record
1. Previous Record
1. Next Record
1. Last Record
1. Show Objects Panel
1. Copies Inputs to Outputs (Only visible if transformer is connected to any object other than writer)
1. Zoom In
1. Zoom Out
1. Zoom back to 100%

## Examples

Example below splits date field into Day, Month and Year using ‘/’ as a delimiter

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-example-1.png" title="Transformer Example 1" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-example-result-1.png" title="Transformer Example Result 1" >}}

Another Example Converts Store Name into More readable format:

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-example-2.png" title="Transformer Example 2" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-example-result-2.png" title="Transformer Example Result 2" >}}

## Auto Mapping

Fill in all necessary data and click map

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/automapping.png" title="Auto Mapping" >}}

## Transformation Functions

- [Transforming Strings]({{<relref "docs/advanced-etl-processor/transformation-functions/strings" >}})
- [Transforming Numbers]({{<relref "docs/advanced-etl-processor/transformation-functions/numbers" >}})
- [Date Transformations]({{<relref "docs/advanced-etl-processor/transformation-functions/dates" >}})
- [Time Transformations]({{<relref "docs/advanced-etl-processor/transformation-functions/times" >}})
- [File Name Transformation functions]({{<relref "docs/advanced-etl-processor/transformation-functions/file-names" >}})
- [Lookup Transformation Functions]({{<relref "docs/advanced-etl-processor/transformation-functions/lookups" >}})
- [XML and HTML Transformation Functions]({{<relref "docs/advanced-etl-processor/transformation-functions/xml-and-html" >}})
- [JSON Transformation Functions]({{<relref "docs/advanced-etl-processor/transformation-functions/json" >}})
- [Regular Expression Transformation Functions]({{<relref "docs/advanced-etl-processor/transformation-functions/regular-expressions" >}})
- [Miscellaneous Transformation Functions]({{<relref "docs/advanced-etl-processor/transformation-functions/miscellaneous" >}})

## Video Tutorial

{{< youtube id="Wd58pvMkpVY" class="ratio ratio-16x9" >}}

{{< aetl >}}
