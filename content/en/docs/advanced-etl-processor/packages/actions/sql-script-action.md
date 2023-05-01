---
author: Peter Jonson
title: SQL Script Action
description: The SQL Script Action runs SQL scripts
draft: false
tags: ['Package', 'Action', 'SQL', 'Script']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

The SQL Script Action runs SQL scripts

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/sql-script-action.png" title="Workflow tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/sql-script-variables.png" title="After execution tab" >}}
\
{{< alert color="secondary">}}Always Use sql nocount on for Microsoft SQL Server Stored Procedures and Scripts{{< /alert >}}

{{< aetl >}}
