---
author: Peter Jonson
title: BrightPearl Reader
description: BrightPearl Reader
draft: false
tags: ['Reader', 'BrightPearl']
date: 2022-09-17

group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About BrightPearl

**Brightpearl** is a fully integrated, web-based business management software system. It allows you to run all your business processes through one piece of software, so you no longer have to suffer the pain of transferring data between multiple different business systems. All your business's information is visible in real-time across every department whether it is entered via your website, inventory control, accounts or CRM.

Until now the only way to prepare data for Data-warehouse was to export data manually. But today with help from [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)it is possible to automate loading data from Brightpearl.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/brightpearl.png" title="Brightpearl" >}}

## Supported data feeds

### brand

https://www.brightpearl.com/developer/latest/product/brand/search.html

### brightpearl-category

https://www.brightpearl.com/developer/latest/product/brightpearl-category/search.html

### contact

https://www.brightpearl.com/developer/latest/contact/contact/search.html

### order

**Search**

https://www.brightpearl.com/developer/latest/order/order/search.html

**List of fields**

https://www.brightpearl.com/developer/latest/order/order/get.html

### option

https://www.brightpearl.com/developer/latest/product/option/search.html

### option-value

https://www.brightpearl.com/developer/latest/product/option%20value/search.html

### product

https://www.brightpearl.com/developer/latest/product/product/search.html

### product-type

https://www.brightpearl.com/developer/latest/product/product-type/search.html

### goods-in-note

https://www.brightpearl.com/developer/latest/warehouse/goods-in-note/search.html

### goods-out-note

https://www.brightpearl.com/developer/latest/warehouse/goods-out-note/search.html

## Additional parameters

Can be passed using search string, as described here

https://www.brightpearl.com/developer/latest/tutorial/working-with-resource-search.html

## Columns

Each resource search supports a set of fixed set of columns - data that will be included in your results like contact names and email addresses. By default, every result will include a value for each column (although that value may be null) it is possible to change the set and order of the columns returned in the results.

It is also possible to constrain the search by specifying one or more column names as query parameters in your resource search URI.

**Example**

primaryEmail=brightpearl.com&firstName=Ben

will only include results where the contact's email address contains brightpearl.com and their first name contains Ben.
