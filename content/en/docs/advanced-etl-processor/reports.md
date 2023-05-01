---
author: Peter Jonson
title: Report
description: A report provides the end-user with the ability to view data as a neatly formatted presentation of data.
draft: false
tags: ['Report']
date: 2023-01-12
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

## Report Designer

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-designer.png" title="Report Designer" >}}

## Report Tool Bar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-toolbar.png" title="Report Tool Bar" >}}

1. Report Properties
1. Notes
1. Saves Report to the Repository
1. Report Connection
1. Show only connections for the current project
1. Manage Versions
1. Add Version
1. Revert to the previous version
1. Make report Read Only

## Creating Basic Report

Select report group from the objects tree and click “new”.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/creating-basic-report.png" title="Creating Basic Report" >}}
\
This will bring up the Report Properties tab as shown. Fill in the description and comment edit box if necessary:
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-properties.png" title="Report Properties" >}}
\
Follow wizard steps

### Report Wizard

{{< image class="mx-auto d-block"  src="/images/active-table-editor/report-wizard.png" title="Report Wizard" >}}

### Data Source

{{< image class="mx-auto d-block"  src="/images/active-table-editor/report-data-source.png" title="Report Data Source" >}}
\
Enter report sql or use query builder

### Query Builder

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/query-builder.png" title="SQL Query Builder" >}}

### Fields Selector

{{< image class="mx-auto d-block"  src="/images/active-table-editor/report-fields.png" title="Report Fields" >}}

### Groups

{{< image class="mx-auto d-block"  src="/images/active-table-editor/report-groups.png" title="Report Groups" >}}

### Layout

{{< image class="mx-auto d-block"  src="/images/active-table-editor/report-layout.png" title="Report Layout" >}}

### Style

{{< image class="mx-auto d-block"  src="/images/active-table-editor/report-style.png" title="Report Style" >}}

Click "Finish" to create the new report

## Report Preview

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-print-preview-button.png" title="Report in Report Designer" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-preview.png" title="Print Preview" >}}
\
Using the preview button, the report can be exported to PDF, Html or into an Excel file as a CSV. Reports can also be emailed, either by saving them into one of the formats stated or directly from the preview facility.

## Passing Parameters into the Report

It is possible to pass parameters into the Report using variables

### Object names

It is very important to use valid object names otherwise variables will not be replaced with the actual value

- For ADO(OleDB) use ADOConnection for connection object and ADOQuery,ADOQuery1...ADOQuery20 for queries
- For UniDac use UNIConnection for connection object and UNIQuery,UNIQuery1...UNIQuery20 for queries
- For BDE use BDEConnection for connection object and BDEQuery,BDEQuery1...BDEQuery20 for queries

### Defining Variables

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-defining-variables.png" title="Defining Variables" >}}

### Defining SQL Parameters:

:P1 is an SQL parameter

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-sql-parameters.png" title="Defining SQL Parameters" >}}

### Linking SQL Parameters to variables

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-sql-parameters-variable-mapping.png" title="Linking SQL Parameters to variables" >}}

### Passing Parameters from Package into the report

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-package-parameters-1.png" title="Passing Parameters from Package into the report" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/report-package-parameters-2.png" title="Passing Parameters from Package into the report" >}}
\
{{< alert color="secondary">}}For string parameters put variable name in quotes{{< /alert >}}

## Notes Dialogue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/notes-dialogues.png" title="Notes Dialogue" >}}

## Video Tutorials

{{< youtube id="OyrxgSWZNzs" class="ratio ratio-16x9" >}}
\
{{< youtube id="EwyxVVxo0O4" class="ratio ratio-16x9" >}}

{{< aetl >}}
