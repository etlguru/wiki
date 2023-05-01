---
author: Maria Salter
title: Calculating Group ID and Record ID
description: This article provides an example of ETL calculation
draft: false
tags: ['Knowledgebase', 'Calculation', 'Script']
date: 2022-09-17
group: knowledgebase-tips
layout: docs
---

## Source Data Example

{{< image class="mx-auto d-block"  src="/images/knowledgebase/source-data-example.png" title="Source data example" >}}

## Desired Result

{{< image class="mx-auto d-block"  src="/images/knowledgebase/calculation-result.png" title="Calculation result" >}}

## Mapping

{{< image class="mx-auto d-block"  src="/images/knowledgebase/mapping.png" title="Mapping" >}}

## Calculating Group ID

{{< image class="mx-auto d-block"  src="/images/knowledgebase/calculation.png" title="Calculation" >}}

```
var sGroupId :string;
sGroupName :string;
begin
sGroupId := GetVariable('vGroupID');
sGroupName := GetVariable('vGroupName');
if sGroupId='' then
begin
SetVariable('vGroupID','0');
SetVariable('vGroupName',[CATEGORYNAME]);
Result:='0';
end
 else if sGroupName<>[CATEGORYNAME] then
begin
sGroupId:=IntToStr(StrToInt(sGroupId)+1);
SetVariable('vGroupID',sGroupId);
SetVariable('vGroupName',[CATEGORYNAME]);
Result:=sGroupId;
end
else
Result:=sGroupId;
end;
```

## Calculating Record ID

```
var sId :string;
sGroupName :string;
begin
sId := GetVariable('vID');
sGroupName := GetVariable('vGroupName1');
if (sId='') or (sGroupName<>[CATEGORYNAME]) then
begin
SetVariable('vID','1');
SetVariable('vGroupName1',[CATEGORYNAME]);
Result:='1';
end
 else
begin
sID:=IntToStr(StrToInt(sID)+1);
SetVariable('vID',sID);
Result:=sID;
end
end;

```

- [Scripting Language]({{<relref "docs/advanced-etl-processor/scripting-language" >}})
- [Best practice for Calculations]({{<ref "best-practice-for-calculations" >}})

{{< aetl >}}
