---
author: Peter Jonson
title: Excel Reader
description: Excel Reader
draft: false
tags: ['Reader', 'Excel']
date: 2022-08-01
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

Data can be extracted from the entire Sheet or just from the data range.

[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) assumes that "Sheet name" and "Range name" are delimited by colon (:).

Users can still call Sheets as a "Great.Victory"

The logic as follows:

- Advanced ETL Processor checks if Great.Victory sheet exits then it will read it
- If it does not exists it will check if Great sheet exits
- If it does exists it will check if Victory range exists if it does It will read data from just Victory range
- If it does not it will read the data from Sheet "Great"

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/excel.png" title="Data Source is an Excel File" >}}
\
{{< alert color="secondary" >}}
Please make sure that the range names are not duplicated within the file
{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/excel-data-range.png" title="Excel Data Range" >}}

Ignore format option

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/ignore_formats.png" title="Ignore format option" >}}
\
{{< alert color="secondary" >}}
Not all formats are supported
{{< /alert >}}

- [How to read a single excel cell value](https://www.etl-tools.com/automation/0004-how-to-read-a-single-excel-cell-value.html)

## Video Tutorial

{{< youtube id="3dNFyvG23gM" class="ratio ratio-16x9" >}}
