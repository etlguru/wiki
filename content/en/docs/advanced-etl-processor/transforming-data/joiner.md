---
author: Peter Jonson
title: Working with Joiner Object
description: Joiner Object joins two data flows.
tags: ['Transformation', 'Joiner']
date: 2022-09-17
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

## About

Joiner Object joins two data flows.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/joiner.png" title="Joiner Object" >}}

## Properties

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/joiner-properties.png" title="Joiner Object Properties" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/joiner-output-fields.png" title="Joiner Object Output Fields" >}}

{{< alert color="secondary">}}There is no need to sort data before joining it. Quite often using lookup transformation object is a faster option.{{< /alert >}}

{{< aetl >}}
