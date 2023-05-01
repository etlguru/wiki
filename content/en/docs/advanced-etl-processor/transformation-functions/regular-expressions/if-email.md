---
author: Peter Jonson
title: If Email
description: Email Address validation that allows both IP addresses and regular domains
draft: false
tags: ['Transformation', 'Transformation Functions', 'Regular Expressions']
date: 2023-02-23
group: advanced-etl-processor-enterprise-regular-expressions-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_email_tranformation_finction.png" title="If Email" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                             |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                                                                                           |
| Description | Email Address validation that allows both IP addresses and regular domains. In the case of an IP address it makes sure that it is no more than 255 for each part. |
| Properties  | Default                                                                                                                                                           |
| Pass        | john@doe.com                                                                                                                                                      |
| Fail        | john@doe                                                                                                                                                          |

{{< /table >}}

{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
