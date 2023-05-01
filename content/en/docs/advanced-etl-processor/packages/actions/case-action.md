---
author: Peter Jonson
title: Case Action
description: Case package action is a convenient way of executing different actions depending on the variable value.
draft: false
tags: ['Package', 'Action', 'Case']
date: 2023-03-18

group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

**Case** package action is a convenient way of executing different actions depending on the variable value.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/case-usage-example.png" title="Case Action usage example" >}}

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/case-action-workflow-1.png" title="Case Action Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/case-action-advanced-2.png" title="Case Action Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/case-variables.png" title="Case Action execution tab" >}}
\
{{< alert color="secondary">}}It is also possible to use calculations in Variable names and Values, for example **{GetSystemDate('YYYYMMDD')}**{{< /alert >}}

{{< aetl >}}
