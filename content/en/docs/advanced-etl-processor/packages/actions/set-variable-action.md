---
author: Peter Jonson
title: Set Variable Package Action
description: Set Variable package action is a convenient way of changing package object properties dynamically
draft: false
tags: ['Package', 'Action', 'Variable']
date: 2022-01-13
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

**Set Variable** package action is a convenient way of changing package object properties dynamically. Once a variable is set, it will be replaced with the actual value of the objects executed after. Package variable name can be any string. It is not recommended to use very short names for package variables, for example, the user can a variable **“I”** and set value to Test. This might create problems later because the letter I will be replaced with “Test” so “C:\Program file” will become “C:\Program f**test**le”

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variable-action-workflow-1.png" title="Workflow tab" >}}

## Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variable-action-example-2.png" title="Variables Action Example" >}}

## Variables tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variable-action-variable-list-3.png" title="After execution tab" >}}
/
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variables-example.png" title="Variables tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variables-variables.png" title="After execution tab" >}}

It is possible to use calculations inside variable by placing calculation inside {}

{{< alert color="secondary">}}Only one pair of {} is allowed{{< /alert >}}

For example:

```
C:\Data{GetSystemDate('YYYYMMDD')}.vis
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/set-variable-calculation.png" title="Set Variable Calculation" >}}

{{< aetl >}}
