---
author: Peter Jonson
title: Dynamic File names
description: Dynamic File names
draft: false
tags: ['Calculations', 'Dynamic File names']
date: 2022-09-09
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

Dynamic file names is a quite common task and there are multiple ways of doing it

## Calculations

It is possible to use calculated filenames by placing calculation inside {}

{{< alert color="secondary" >}}
Only one pair of {} is allowed
{{< /alert >}}

## Example

This will use today date to generate the filename

{{< command >}}
C:\Data\{GetSystemDate('YYYYMMDD')}.txt
{{< /command >}}

and that one will use yesterdays date

{{< command >}}
C:\Data\{DecDateS(GetSystemDate('YYYYMMDD'),'YYYYMMDD','DAY',1)}.txt
{{< /command >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/dynamic-file-names.png" title="Dynamic file names" >}}

## Variables

```
<CommonDocumentsDir>\DBSL\{GetSystemVariable('SOURCE_FILE_NAME')}.txt
```

```
<CommonDocumentsDir> is a variable and will be replaced with an actual value before execution
```

```
C:\Data\{GetVariable('<file_name>')}.txt
```

## More complex example

This calculation will create a new file every time [F001] is changed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/dinamic-file-names.png" title="Dynamic Filenames" >}}

```
begin
if GetVariable('<file_name>')<>[F001] then // record changed
 begin
  SetVariable('<file_name>',[F001]);
  SourceChanged; // creating new file
 end;
 Result:='test';
end;
```

{{< alert color="secondary" >}}
Default repository has a number of useful examples
{{< /alert >}}

[Building a complex file name](https://www.etl-tools.com/forum/data-warehousing-and-data-integration/8735-building-a-complex-file-name.html)

{{< aetl >}}
