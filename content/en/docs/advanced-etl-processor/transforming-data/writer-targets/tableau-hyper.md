---
author: Peter Jonson
title: Tableau Hyper Writer
description: Tableau Hyper Writer
draft: false
tags: ['Writer', 'Tableau', 'Hyper']
date: 2022-08-01

group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

## About Tableau

Tableau is a business intelligence software that allows anyone to connect to data in a few clicks, then visualize and create interactive, shareable dashboards with a few more. It's easy enough that any Excel user can learn it, but powerful enough to satisfy even the most complex analytical problems. Securely sharing your findings with others only takes seconds.

The result is BI software that you can trust to actually deliver answers to the people that need them.

http://www.tableausoftware.com/business-intelligence

## What’s Hyper?

Under the hood, Hyper is the technology that now powers Tableau’s data engine. The data engine is what handles opening, creating, refreshing, and querying your extracts.

https://www.tableau.com/about/blog/2018/1/extracts-hyper-speed-what-you-need-know-79397

**More information about tableau field types**

https://help.tableau.com/current/api/hyper_api/en-us/reference/sql/datatype.html

## Adding data to an existing hyper table

To add data open writer properties dialogue and select an existing table from the drop-down box

## Creating new hyper table

Open writer properties dialogue and enter new table name.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/tableau_hyper_1.png" title="Tableau Hyper" >}}

Define Table structure

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/creating_hyper_file.png" title="Creating Hyper File" >}}
\
{{< alert color="secondary">}}If hyper file exists the reader will take the field lists from the file otherwise the user have to define/change it manually {{< /alert >}}

Run Transformation and check that table was created

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/creating_hyper_file_log.png" title="Creating Hyper File Log" >}}

## Running SQL against hyper database

It is possible to run SQL before and after loading the data.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/tableau_hyper_execute_sql_1.png" title="Tableau Hyper Execute Sql" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/tableau_hyper_execute_sql_2.png" title="Tableau Hyper Execute Sql" >}}

{{< alert color="secondary">}}Working with hyper files requires 64-bit version{{< /alert >}}

## Video Tutorials

{{< youtube id="Xayxv9IHICU" class="ratio ratio-16x9" >}}
\
{{< youtube id="eK-KRvI5L_Y" class="ratio ratio-16x9" >}}

{{< aetl >}}
