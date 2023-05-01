---
author: Peter Jonson
title: Working with Date fields
description: How to load data into date fields
draft: false
tags: ['Import', 'Date']
date: 2022-10-22
group: 'advanced-etl-processor-enterprise-import-how-to'
menu: advanced-etl-processor-enterprise
layout: docs
weight: 6
---

In order to load data into date or time fields date format must be provided for the source field.
Our ETL Software automatically converts data into the format required for the target database.

## Performance tips

- Applying date/time format is a very processor-intensive operation,
- Shorter formats are faster,
- Formats with no months names are faster as well,
- dd/mm/yyyy is faster than d/m/yy.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/import/date-formats.png" title="Import Date Formats" >}}

- Various formats can be selected using drop-down box
- If the format is missing it can be entered

{{< alert color="secondary" >}}
The full list of date formats can be found [here:]({{<relref "docs/advanced-etl-processor/date-formats" >}})
{{< /alert >}}

Important thing is to understand that this format has nothing to do with your target database.
This is the format of the source data. It is there to help to convert a string into date-time type
inside of the software, so it can be loaded later into the date or timestamp field

## Video Tutorial

{{< youtube id="T3hYsbeAw74" class="ratio ratio-16x9" >}}

{{< aetl >}}
