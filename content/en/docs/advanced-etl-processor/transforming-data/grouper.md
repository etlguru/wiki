---
author: Peter Jonson
title: Working with Grouper
description: Working with Grouper
draft: false
tags: ['Transformation', 'Grouper']
date: 2022-09-17
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/grouper.png" title="Grouper" >}}

To change grouper properties double click on the object. Choose appropriate grouping order and grouping type. Fields with grouping type Ignore are not passed to the next object.

{{< alert color="secondary">}}Grouper does not perform sorting, it is recommended to sort data first{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/grouper-properties.png" title="Grouper Properties" >}}

{{< aetl >}}
