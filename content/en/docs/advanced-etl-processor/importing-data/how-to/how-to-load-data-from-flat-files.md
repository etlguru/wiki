---
author: Peter Jonson
title: Loading data from a Flat File(s)
description: How to load data from a Flat File
draft: false
tags: ['Import', 'Flat File']
date: 2022-08-01
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 1
---

## Supported a Flat File(s) formats

Data can be loaded from ASCII and Unicode files in UTf8, UTF16BE and UTF16LE formats with BOM marker and without
\
{{< alert color="secondary" >}}
Unicode is a computing industry standard allowing computers to consistently represent and manipulate text expressed in most of the world's writing systems.
{{< /alert >}}

To perform data mapping:

- Click Data Target Options button

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/main5.png" title="Data Target Options" >}}

- Dialog box will appear
- Select appropriate target type

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datatartget.png" title="Data Target" >}}

- Click Get tables list
- Select Table you would like to import data into from the Drop Down List

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datatarget-odbc3.png" title="Data Target ODBC" >}}

- Click Transformation tab
- Select Add Records
- Click OK
- Click Data Source Option Button

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/html-toolbar2.png" title="HTML toolbar" >}}

- Dialog box will Appear

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datasource-options-text.png" title="Datasource-options" >}}

- Set Delimiter and Quota to appropriate values

Note: If you want to load data from several files specify a mask.

Click OK. Click and select the file you would like to import data from. {{< image src="/images/etl/advanced-etl-processor/import/search-icon.png" title="File Selector" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/source-text2.png" title="Search" >}}

- Select Fist field in the Data Target fields list and drag and drop it above [F1] field.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/main5.png" title="Mapping" >}}

You may change field mapping by using the mapping panel at any time.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/mapping.png" title="Mapping" >}}

## How to perform Auto mapping

If the Data Source and Data Target have got the same fields’ names you may use the Automap feature.

Click {{< image src="/images/etl/advanced-etl-processor/import/toolbar-button.png" title="Automap" >}} , Fill in all necessary data and click map.

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/import/automap.png" title="Automap" >}}
/
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/import/source-text.png" title="Automap" >}}

Now we are ready to import data.\
Let’s check the script first.\
(Click to check the script) {{< image src="/images/etl/advanced-etl-processor/import/checkscript-button.png" title="Check script" >}}

Here is an example of the error, the date format is missing.

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/import/target-field-format-date.png" title="Target field format date" >}}

Click to load data into the database {{< image src="/images/etl/advanced-etl-processor/import/run-button.png" title="Run button" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/processing-data.png" title="Processing Data" >}}
\
Once loading is finished you may check the Log file or the Rejected records file.

### Video Tutorial

{{< youtube id="ts676kkTR-Q" class="ratio ratio-16x9" >}}

{{< aetl >}}
