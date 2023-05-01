---
author: Peter Jonson
title: Performing Calculations
description: How to perform ETL calculations during import
draft: false
tags: ['Import', 'Calculation']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 5
---

## Simple calculation

To perform a simple calculation set mapping type to calculation and type constant or formula into calculation edit box

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/mapping1.png" title="Manual Mapping" >}}

## Multiplying fields

```
StrToFloat([INTEGER_F])\* StrToFloat([FLOAT_F])
```

{{< alert color="secondary">}}[INTEGER_F] and [FLOAT_F] are source fields names{{< /alert >}}

## Concatenation

```
[INTEGER_F]+ kilos"
```

## More complicated examples

```
Iif(StrToFloat([FLOAT_F])> StrToFloat([INTEGER_F]),1,2)
Trim('[CHAR_F]')
```

The good starting point is an Expression Editor.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/expression-editor-uppercase.png" title="Expression Editor" >}}

## More information about scripting language

- [Date formats]({{<relref "docs/advanced-etl-processor/date-formats" >}})
- [Scripting Language]({{<relref "docs/advanced-etl-processor/scripting-language" >}})
- [Best practice for calculations]({{<relref "/knowledgebase/tips/best-practice-for-calculations" >}})

{{< aetl >}}
