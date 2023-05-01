---
author: Peter Jonson
title: Text Reader
description: Text Reader
draft: false
tags: ['Reader', 'Text', 'Flat File']
date: 2022-05-11
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

The Reader is capable of extracting data from delimited or fixed-width files. All parameters are user-definable. It can also skip a number of Header and Footer lines

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data-reader-properties-text.png" title="Data Reader Properties" >}}

The Text tab defines the format of the source text file.

{{< alert color="secondary" >}}
Note: it is extremely important to specify a correct Line terminator otherwise the application may hang when working with very large text files
{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data-reader-data-reading-restrictions.png" title="Data Reading Restrictions" >}}

The Data Reading Restriction tab can be used to speed up testing while working with a very large file or table.

The Rejected records file can have a pre-defined format. The Rejected File tab allows the user to set this up.
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data-reader-rejected-file-format.png" title="Rejected File" >}}

## Data View

One of the useful features of the [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) is the ability to view the resultant data prior, or subsequently processed. The data view looks like a spreadsheet view as follows:
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data-view-spreadsheet.png" title="Data View" >}}

## Data View Toolbar

The data view toolbar allows you to change various aspects of the data view, such as refreshing data as it changes and setting properties for how the data will look. You can also switch between viewing of the data and checking to see how the data is defined i.e. the data dictionary, via the “Switch to Data Definition View”.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/data-view-toolbar.png" title="Data View Toolbar" >}}

1. Reader Properties
1. Refresh Data
1. Edit file in an external editor
1. Swap Reader and Writer
1. Add a new column
1. Delete the last column
1. Switch to Data View
1. Switch to Data Definition View

## Data Definition View

Note: You may rename fields and change the field’s width here. (Works only for text files)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data-definition-view.png" title="Data Definition View" >}}

## Data Definition View Toolbar

Within the Data Definition view, you can perform a number of actions. These allow you to change how you want data to be represented in the data view screens. The navigation also allows switching between views.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data-definition-view-toolbar.png" title="Data Definition View Toolbar" >}}

1. Reader Properties
1. Refresh Data
1. Print Data Definition
1. Print Preview Data Definition
1. Find
1. Edit file in an external editor
1. Add a new column
1. Delete the last column
1. Switch to Data View
1. Switch to Data Definition View

## Popup Menu

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/popup-menu.png" title="Popup Menu" >}}

- Set Field’s Names takes field names from a certain file line.
- It is also possible to copy and paste fields from excel

## Video Tutorials

{{< youtube id="klNGkEfYggM" class="ratio ratio-16x9" >}}
\
{{< youtube id="FCS1Z6JqKh4" class="ratio ratio-16x9" >}}
