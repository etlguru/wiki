---
author: Maria Salter
title: Inserting context of the file inside email message text
description: Lean how to insert context of the file inside email message text
draft: false
tags: ['Knowledgebase', 'EMail', 'Automation', 'Variables']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## Here is very basic example of email automation

This is an important feedback message stored on the file which must be passed to the supplier

{{< image class="mx-auto d-block"  src="/images/knowledgebase/insert-file-1.png" title="Email Automation" >}}

## Automation Package

{{< image class="mx-auto d-block"  src="/images/knowledgebase/insert-file-2.png" title="Automation Package" >}}

## Script Package Action

{{< image class="mx-auto d-block"  src="/images/knowledgebase/insert-file-3.png" title="Script Package Action" >}}

```
begin
SetVariable('',FileToString('C:\tmp\text.txt'));
Result:=True;
end;
```

## Send Email Action

{{< image class="mx-auto d-block"  src="/images/knowledgebase/insert-file-4.png" title="Send Email Action" >}}

## Variable Value after script execution is completed

{{< image class="mx-auto d-block"  src="/images/knowledgebase/insert-file-5.png" title="Variable Value" >}}

## About Variables

Variables are used to pass parameters between various objects.\
For example, SQL script has failed and you would like to email the SQL to the developer.\
Insert \<Sql Script> Into email message and it will be replaced with actual SQL.

**Note**

There are several ways to create variables

- Using script action
- Using transformation action
- Using calculation object within transformation action or package
- Using Set Variable Action
- Manually using Global Variables

{{< aetl >}}
