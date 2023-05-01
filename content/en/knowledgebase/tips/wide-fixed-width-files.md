---
author: Maria Salter
title: Working with very wide fixed width files
description: This article describes how to work with very wide text files
draft: false
tags: ['Knowledgebase', 'Text']
date: 2022-08-01
group: knowledgebase-tips
layout: docs
---

## A Question from the Customer:

I'm trying to set up the reader for a fixed-width file with 900 columns. I have a layout file with the column names and field widths: The widths are the 3rd row of the reader file.
If there was a way to paste or load the definition into the data definition view that would be great.
Is there any easy way to do this? I'm not going to type in 900 field widths. My best current idea is to create a table via SQL script, set the writer to look at that and use and copy the definition to the reader.

https://www.etl-tools.com/forum/advanced-etl-processor/8651-fixed-width-file-reader-definition.html

## Answer:

Click on data reader.
Right-click in the middle of the data grid and select "Set number of fields"

{{< image class="mx-auto d-block"  src="/images/knowledgebase/fixedwidth1.png" title="Working with very wide fixed width files" >}}

Enter the number of fields

{{< image class="mx-auto d-block"  src="/images/knowledgebase/fixedwidth2.png" title="Working with very wide fixed width files" >}}

Click on data definition, click select all and then copy

{{< image class="mx-auto d-block"  src="/images/knowledgebase/fixedwidth3.png" title="Working with very wide fixed width files" >}}

Paste data into Excel and edit field names and widths\
Copy data from excel back into Advanced ETL Processor\
(Select fist cell fist, then select all and paste data)

{{< image class="mx-auto d-block"  src="/images/knowledgebase/fixedwidth4.png" title="Working with very wide fixed width files" >}}
\
{{< alert color="secondary">}}If you have too many fields use [Fields Selector Object]({{<relref "docs/advanced-etl-processor/transforming-data/fields-selector" >}}) to filter the ones you need {{< /alert >}}

## Video Tutorial

{{< youtube id="FCS1Z6JqKh4" class="ratio ratio-16x9" >}}

{{< aetl >}}
