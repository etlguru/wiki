---
author: Peter Jonson
title: SQL Scripts
description: SQL Scripts
draft: false
tags: ['SQL']
date: 2023-07-06
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

## Properties Dialogue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/sql-script-properties.png" title="SQL Scripts Properties" >}}
\
{{< alert color="secondary">}}To edit script double click on any previously created SQL Scripts.
{{< /alert >}}

## SQL Script

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/sql-script-run.png" title="SQL Script" >}}
\
{{< alert color="danger" >}}
**Note:** Please always remove comments from SQL  
{{< /alert >}}

## Tool Bar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/sql-script-toolbar-1.png" title="SQL Script" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/sql-script-toolbar-2.png" title="SQL Script Toolbar" >}}

1. SQL Script Properties
1. Notes
1. Load the SQL script from the disk
1. Save the SQL script to the disk
1. Save the SQL Script to the repository
1. Print the SQL script
1. Preview
1. Cut
1. Copy
1. Paste
1. Undo
1. Completion Proposal
1. Search
1. Repeat Search
1. Find Previous
1. Replace
1. Execute SQL Script
1. Stop execution when an error happens
1. SQL script separator
1. Connection
1. Show connections only for current project
1. Show/hide log
1. View Execution Log (When executed within the package or by agent/scheduler)
1. Schedule for execution
1. Manage Versions
1. Add Version
1. Revert to previous version
1. Make SQL Script read-only
1. Browse data

{{< alert color="secondary">}}
Use set sql nocount on for Microsoft SQL Server Stored Procedures and Scripts
SQL Script supports both package and global variables
Always remove comments from SQL  
{{< /alert >}}

## Version Control

Every time the user presses save button package is automatically added to the version control

- [Version Control]({{<relref "docs/advanced-etl-processor/version-control" >}})

{{< aetl >}}
