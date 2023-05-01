---
author: Maria Salter
title: SalesForce Bulk API
description: This article describes how to check SalesForce Bullk Load status
draft: false
tags: ['Knowledgebase', 'SalesForce']
date: 2022-09-17
group: knowledgebase-tips
layout: docs
---

## Enabling SalesForce Bulk API

{{< image class="mx-auto d-block"  src="/images/knowledgebase/salesforce1.png" title="SalesForce" >}}

## Checking SalesForce Bulk Data Load Job Status

- Login to SalesForce
- Click monitoring
- Click Bulk Data Load Jobs

{{< image class="mx-auto d-block"  src="/images/knowledgebase/salesforce2.png" title="Checking SalesForce Bulk Data Load Job Status" >}}

- Click on Job Id

{{< image class="mx-auto d-block"  src="/images/knowledgebase/salesforce3.png" title="Job Id" >}}

- Check records processed and failed
- Click view results to inspect the errors

{{< image class="mx-auto d-block"  src="/images/knowledgebase/salesforce4.png" title="Checking SalesForce Bulk Data Load Job Status" >}}

## SalesForce Bulk API Limitations

- Batches for data loads can consist of a single CSV, XML, or JSON file that is no larger than 10 MB.
- A batch can contain a maximum of 10,000 records.
- A batch can contain a maximum of 10,000,000 characters for all the data in a batch.
- A field can contain a maximum of 32,000 characters.
- A record can contain a maximum of 5,000 fields.
- A record can contain a maximum of 400,000 characters for all its fields.
- A batch must contain some content or an error occurs.

More Information can be found here

(Bulk API Limitations)[https://developer.salesforce.com/docs/atlas.en-us.api_asynch.meta/api_asynch/asynch_api_concepts_limits.htm]

{{< aetl >}}
