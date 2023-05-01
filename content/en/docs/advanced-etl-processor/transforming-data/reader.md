---
author: Peter Jonson
title: Working with Reader
description: The Reader extracts data from various data sources.
draft: false
tags: ['Transformation', 'Reader']
date: 2022-09-17
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

## About Reader

The Reader extracts data from various data sources.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/reader.png" title="Reader Options" >}}

Every Transformation created must have one or more reader objects. The Reader connects to the Data source and extracts data from it. Depending on the Data source type some options may not be available. To change the Reader properties double-click on the Reader object. Readers are executed sequentially.

## Universal Data Reader

One of the benefits of using [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)is a concept of Universal Data Reader

Consider the following scenario:

You have several extracts from your accounting system

- Text files
- Excel Files
- Access Databases

All files have the same format such as:

- Same field’s order
- Same field’s names
- Same date and number formats

Provided that you are using [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) all you need to do is to change the connection type no mapping will be lost.

Other tools use a different connector for different databases and some of them even sell separate licenses for them. That means that the user has to recreate the mapping for new files/databases.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data-reader-properties.png" title="Reader Data Sources" >}}

## Video Tutorials

{{< youtube id="klNGkEfYggM" class="ratio ratio-16x9" >}}
\
{{< youtube id="FCS1Z6JqKh4" class="ratio ratio-16x9" >}}

{{< aetl >}}
