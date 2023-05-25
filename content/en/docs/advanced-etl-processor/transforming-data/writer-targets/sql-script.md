---
author: Peter Jonson
title: Running SQL Scripts
description: Running SQL Scripts
draft: false
tags: ['Writer', 'SQL', 'Scripts']
date: 2022-09-24
group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

SQL Scripts can be run before and after the transformation.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/sql-editor-menu.png" title="SQL Editor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/sql-editor.png" title="Execution Log" >}}

## SQL Editor Toolbar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/sql-edit-toolbar.png" title="SQL Editor Toolbar" >}}

1. Load Script from a file
1. Save Script to a file
1. Print
1. Print Preview
1. Clear Script
1. Cut
1. Copy
1. Paste
1. Undo
1. Clear
1. Enable autocomplete
1. Find
1. Find Next
1. Find Previous
1. Replace
1. Run
1. Stop on error
1. Show/Hide Log

{{< alert color="secondary">}}
Always Use set sql nocount on for Microsoft SQL Server Stored Procedures and Scripts
Also remove comments from SQL
{{< /alert >}}

{{< aetl >}}
