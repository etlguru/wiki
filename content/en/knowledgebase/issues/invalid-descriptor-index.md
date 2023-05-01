---
author: Maria Salter
title: Invalid Descriptor Index
description: 'How to fix SQLGetDataA Failed: Invalid Descriptor Index'
draft: false
tags: ['Knowledgebase', 'SQLGetData', 'Error', 'ODBC', 'Blob']
date: 2022-08-01
group: knowledgebase-issues
layout: docs
---

## Problem

Getting "SQLGetDataA Failed: Invalid Descriptor Index" Error

{{< image class="mx-auto d-block"  src="/images/knowledgebase/invalid-descriptor-index-error.png" title="Invalid Descriptor Index Error" >}}

## Solution

The blob, text, ntext, varchar (max) etc., must be the last field in source SQL.

## Example

Set source type to SQL then use select normal fields, blob fields from a table as source SQL.

## Video Tutorial

{{< youtube id="lu7jNId3S-0" class="ratio ratio-16x9" >}}

{{< aetl >}}
