---
author: Maria Salter
title: Processing files based on modification date
description: This article demonstrates processing files based on modification date
draft: false
tags: ['Knowledgebase', 'Transformation']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## Question from the customer

I would like to pick a specific file on a different server at a particular time if it was modified in the last 2 hrs and load data from it into the database. If the file was not updated in the last 2 hrs a mail needs to be sent to the responsible personnel.

## Solution

There are several ways of doing it, as usual, you can write a script to check the modification date or you can use transformations for it. Transformation is an easier option. Create two transformations First, one will be used to check file modification date Second one for loading the data.

## Checking file modification date

Set DataReader source type to File System and enter the file name into the mask box.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/datareader-properties-1.png" title="Data Reader Properties" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/transformation-2.png" title="Transformation" >}}

Open Validator and create validation as in the picture below The logic is very simple We use to compare the value to check if modified date is less than two hours ago and if it is we set the result to true Then we use Is Equal to abort execution

{{< image class="mx-auto d-block"  src="/images/knowledgebase/validator-3.png" title="Validator" >}}

## Objects Properties

{{< image class="mx-auto d-block"  src="/images/knowledgebase/change-date-properties.png" title="Change Date Properties" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/compare-values-properties.png" title="Change Value Properties" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/isequaltoproperties-6.png" title="Is Equal To Properties" >}}

## Package

{{< image class="mx-auto d-block"  src="/images/knowledgebase/package-7.png" title="Package" >}}
\
{{< alert color="secondary" >}}The file might be locked for editing so we try to copy it first{{< /alert >}}

{{< aetl >}}
