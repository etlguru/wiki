---
author: Peter Jonson
title: Filtering data
description: How to filter data
draft: false
tags: ['Import']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 5
---

When data source is a database best way to filter data is to use where statement for files is filter expression

Click filter button to build filter expression

## Basic Filter

Load data for specific customer

```
[RECORDTYPE]=1
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/filter.png" title="Data filter" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/expression-editor.png" title="Expression Builder" >}}

## Multiple criteria filter

```
([RECORDTYPE]=1) or ([RECORDTYPE]=56)
```

\
{{< alert color="secondary">}}Add brackets for complex expressions{{< /alert >}}

{{< aetl >}}
