---
author: Peter Jonson
title: Loading data from an ODBC Data Source
description: How to load data from an ODBC Data Source
draft: false
tags: ['Import', 'ODBC']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 2
---

Data mapping for ODBC is very similar to the [Loading data from a Flat File(s)]({{<ref "how-to-load-data-from-flat-files" >}})

- Click Data Source Option Button.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/html-toolbar2.png" title="Toolbar" >}}

- Dialog box will appear.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datasource-options-odbc-selected.png" title="ODBC" >}}

- Set Data Source Type to ‘ODBC’.

- Select ODBC DSN from the Drop Down List or alternatively create a new ODBC DSN or modify the old one by using ODBC administrator.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datasource-options-odbc1.png" title="DataSource Options ODBC" >}}

- Fill in Username and Password if required.
- Click Update Tables List.
- Specify tables you want to load data from or alternatively type mask to find tables automatically every time you import data.
- Click OK.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/datasource-tables.png" title="DataSource Tables" >}}

- Select a table you want to see from the drop-down box.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/source-grid.png" title="Source Grid" >}}

- Map fields

[List of ODBC Drivers Download Links]({{<relref "/knowledgebase/tips/list-of-odbc-drivers-download-links" >}})

{{< aetl >}}
