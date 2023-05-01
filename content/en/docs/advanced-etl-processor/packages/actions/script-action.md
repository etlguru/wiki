---
author: Peter Jonson
title: Script Action
description: Script package action allows writing additional complicated checks and validations.
draft: false
tags: ['Package', 'Action', 'Script', 'Pascal', 'Python']
date: 2023-03-18

group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

**Script** package action allows writing additional complicated checks and validations.

Two languages are supported:

- Pascal Script
- Python

## Pascal Script Example

```pascal
Var I : Integer;
begin
 I:=1;
 SetVariable('I',I);
 I:=GetVariable('I');
 WriteToLog('Error',I);
 Result:=True;
end;
```

```
Result:=True; => Success
Result:=False; => Failure
```

## Python Example

```python
import etltools
etltools.SetVariable('<Time>',15)
s=etltools.GetVariable('<Name>')
etltools.WriteToLog('Done')
Result.Value = 0
```

```
Result.Value = 1 => Success
Result.Value = 0 => Failure
```

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/script-action-properties-1.png" title="Workflow tab" >}}
\
{{< alert color="secondary">}}Expression builder only works with Pascal script{{< /alert >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/script-action-expression-builder-2.png" title="Advanced tab" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/script-action-expression-editor-3.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/script-action-variables.png" title="After execution tab" >}}

- [Date Formats]({{<relref "docs/advanced-etl-processor/date-formats" >}})
- [Supported Functions List]({{<ref "supported-functions-list" >}})
- [Best Practice for Calculations]({{<relref "/knowledgebase/tips/best-practice-for-calculations" >}})
- [Scripting Language]({{<relref "docs/advanced-etl-processor/scripting-language" >}})
- [Working with python]({{<ref "working-with-python" >}})
- [Download Python](https://www.python.org/downloads)

{{< aetl >}}
