---
author: Peter Jonson
title: Loading data from Excel/Access/Dbf File(s)
description: How to load data from an Excel/DBF Access File
draft: false
tags: ['Import', 'Excel', 'Access', 'Dbf']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 4
---

Data mapping for Excel file is very similar to the [Loading data from a Flat File(s)]({{<ref "how-to-load-data-from-flat-files" >}})

- Click Data Source Option Button.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/html-toolbar2.png" title="Toolbar" >}}

- Dialog box will appear.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datasource-options.png" title="Datasource Options" >}}

- Select appropriate Data source type.
- Select appropriate version of Access/Excel if necessary

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datasource-options-excel.png" title="Datasource Options Excel" >}}

- Click and select the file you would like to load. {{< image src="/images/etl/advanced-etl-processor/import/search-icon.png" title="File Selector" >}}

- Select Table to load data from
- Click OK.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/source-excel-file.png" title="Source Excel File" >}}

Note: Specify mask to load data from several files/tables.

{{< aetl >}}
