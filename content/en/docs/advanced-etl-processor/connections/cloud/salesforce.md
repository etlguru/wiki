---
author: Peter Jonson
title: SalesForce Connection
description: SalesForce Connection
draft: false
tags: ['Connection', 'Cloud', 'SalesForce']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-cloud-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/sales-force-connection-properties.png" title="SalesForce Connection" >}}

## Creating SalesForce connection

- In the Name Text Box type in a new name for the SalesForce connection you are about to create
- Type in Customer Key
- Type in Customer Secret
- Type in Security Token
- Type in Username
- Type in Password
- Test the connection
- Click OK to close the SalesForce connection properties window

## Getting Consumer Key and Consumer Secret

- Login to SalesForce
- Click develop
- Click Remote access authentication.

## Getting security token

- Click my personal information,
- Reset security token.

SalesForce support subset of SQL More information can be found here:

[https://www.salesforce.com/us/developer/docs/api/index_Left.htm#CSHID=sforce_api_calls_soql.htm](Sales Force Documentation)

## Additional Information

- [Connecting to SalesForce]({{<ref "/knowledgebase/connections/connecting-to-salesforce" >}})
- [SalesForce Bulk API]({{<ref "/knowledgebase/tips/salesforce-bulk-api" >}})

{{< aetl >}}
