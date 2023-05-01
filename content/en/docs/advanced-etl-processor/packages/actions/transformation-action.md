---
author: Peter Jonson
title: Transformation Action
description: Transformation Package Action
draft: false
tags: ['Package', 'Action', 'Transformation']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/transformation-action.png" title="Workflow tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/transformation-action-variables.png" title="After execution tab" >}}

```
Variables <Transformation Processed>,<Transformation Errors>,<Transformation Rejected>,<Transformation Records/Sec> are created for every data reader (<Transformation Processed 1> etc)
<Transformation Writer Errors> a total number for all data writers
<Transformation Error> holds generic error description (file not found for example)
```

- [Designing Transformations]({{<relref "docs/advanced-etl-processor/transforming-data/getting-started" >}})
- [Mapping Screen]({{<relref "docs/advanced-etl-processor/transforming-data/screen-overview" >}})

{{< aetl >}}
