---
author: Peter Jonson
title: Creating New Import
description: In order to load data from the data source into the data target, the user must define data mapping between the target table and data source.
draft: false
tags: ['Import']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-import-getting-started'
menu: advanced-etl-processor-enterprise
layout: docs
---

In order to load data from the data source into the data target, the user must define data mapping between the target table and data source.

{{< alert color="secondary">}}The simplest way to create an Import script is to use the import script wizard.{{< /alert >}}

- Click System Menu→New→Import.
- Fill in the Description edit box with the name of an Import you are about to create.
- Follow wizard Instructions

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/import-script-wizard.png" title="Import Script Wizard" >}}

## Mapping Screen Overview

- Double click on any demo Import.
- Import editor will appear

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/mapping-screen-overview.png" title="Screen Overview" >}}

## Main tool bar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/main-tool-bar.png" title="Main Toolbar" >}}

1. Data Target options
2. Loads Import Script From the file
3. Saves Import Script to the file
4. Saves as
5. Saves Import to the Repository
6. Refreshes fields list fro the database
7. Checks Import for mapping errors
8. Data preview
9. Allows the user to clear field mapping
10. Hides mapping panel
11. Data Import
12. Manage Versions
13. Add Version
14. Revert to the previous version
15. Make import ReadOnly

## Source tool bar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/mapping-source-toolbar.png" title="Source tool bar" >}}

1. Data source options
2. Refreshes Source data
3. Adds new column
4. Deletes last column
5. Auto map the source fields to the target fields
6. Filter
7. Records to Show
8. Sources file name/ table name

## Mapping panel

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/mapping-panel.png" title="Mapping panel" >}}

Mapping panel provides the user with all information related to the mapping of one particular field.
There are two ways of mapping: direct and through calculations.

Alternately you may hide Mapping panel and use grid to perform the mapping. See the picture below

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/user-mapping-panel1.png" title="Mapping panel" >}}

## SQL Statements

SQL statements can be run before and after data import.

- In order to Execute several SQL statements user must specify SQL delimiter
- SQL statements are run against target connection
- No select statements allowed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/sql-tab.png" title="SQL Statements" >}}

## Template tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/user-template-tab.png" title="Template tab" >}}

## Import Log Tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/transformation-log.png" title="Import Log Tab" >}}

## Rejected Records Tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/user-rejected-records-tab.png" title="Rejected Records Tab" >}}

{{< aetl >}}
