---
author: Peter Jonson
title: User Input
description: Asks User to provide information during package execution.
draft: false
tags: ['Package', 'Action']
date: 2023-06-05
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

User Input package action is used for debugging.

## Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/user-input-example.png" title="Workflow tab" >}}
\
{{< alert color="warning">}}User Input does not work when the agent is used for execution or in a separate thread{{< /alert >}}

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/user-input-properties.png" title="Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/user-input-advanced.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/user-input-variables.png" title="After execution tab" >}}

{{< aetl >}}
