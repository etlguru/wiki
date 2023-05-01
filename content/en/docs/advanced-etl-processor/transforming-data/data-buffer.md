---
author: Peter Jonson
title: Working with Data Buffer Object
description: Data buffer does not pass any data to the next transformation object until execution of the previous transformation object completed successfully.
draft: false
tags: ['Transformation', 'Data Buffer']
date: 2022-09-17

group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/data-buffer.png" title="Working with Data Buffer Object" >}}
\
It acts as a buffer and does not pass any data to the next object until execution of the previous object completed successfully.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/data-buffer-object-properties.png" title="Working with Data Buffer Object" >}}
\
It can be used when you are validating very large file but you only want to load data only if file passes the validation or when you are loading data into multiple tables and want to load fact table last.

## Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/data-buffer-object-usage-example.png" title="Data Buffer Object Example" >}}

Validator aborted execution and no records were written by the writer.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/data-buffer-object-usage-example1.png" title="Data Buffer Object Example" >}}

## Log

```
Information 27/06/2018 12:24:05 PM Preparing Writers...
Information 27/06/2018 12:24:05 PM Writer: {Writer3} Connection Type is: Text
Information 27/06/2018 12:24:05 PM Writer: {Writer3} Writer { Writer3 } Is Ready
Information 27/06/2018 12:24:05 PM All Writers are Ready
Information 27/06/2018 12:24:05 PM Target file: C:\DEMO\Buffer\result.csv
Information 27/06/2018 12:24:05 PM Processing Data...
Information 27/06/2018 12:24:05 PM Reader:{Reader} Connection Type is: Text
Information 27/06/2018 12:24:05 PM Reader:{Reader} Path: C:\DEMO\Text Files
Information 27/06/2018 12:24:05 PM Reader:{Reader} Mask: Orders.csv
Information 27/06/2018 12:24:05 PM Reader:{Reader} Found: 1 files to read
Information 27/06/2018 12:24:05 PM Reader:{Reader} Reading all files
Information 27/06/2018 12:24:05 PM Reader:{Reader} Source File: C:\DEMO\Text Files\Orders.csv
Information 27/06/2018 12:24:05 PM 1 Data Buffer: Validation Reading Data Into the buffer
Information 27/06/2018 12:24:05 PM 1 Data Buffer: Validation Buffer size: 20,003
Error 27/06/2018 12:24:05 PM 1997 Is Equal To:{} Execution Aborted: Value of Field [ORDERNO] is 2000. Execution Result of Function 'Is Equal To' is Success
```

{{< aetl >}}
