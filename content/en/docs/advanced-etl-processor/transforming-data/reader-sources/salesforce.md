---
author: Peter Jonson
title: SalesForce Reader
description: SalesForce Reader
draft: false
tags: ['Reader', 'SalesForce']
date: 2022-09-17
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/salesforce.png" title="RSS Feed Reader" >}}

**Note:**

SalesForce support subset of SQL more information can be found here:

[SalesForce SQL](https://www.salesforce.com/us/developer/docs/api/index_Left.htm#CSHID=sforce_api_calls_soql.htm)

About “Use Query All” option: SFDC WebServices API documentation describing the queryAll() method:"You can use queryAll() to query on all Task and Event records, archived or not. You can also filter on the isArchived field to find only the archived objects. You cannot use query() as it automatically filters out all records where isArchived is set to true. You can update or delete archived records, though you cannot update the isArchived field. If you use the API to insert activities that meet the criteria listed below, the activities will be archived during the next run of the archival background process."

- [Connecting to SalesForce]({{<ref "/knowledgebase/connections/connecting-to-salesforce" >}})
- [SalesForce Bulk API]({{<ref "/knowledgebase/tips/salesforce-bulk-api" >}})
