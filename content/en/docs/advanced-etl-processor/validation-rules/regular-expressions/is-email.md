---
author: Peter Jonson
title: Is Email
description: Email Address validation that allows both IP addresses and regular domains. In the case of an IP address it makes sure that it is no more than 255 for each part.
draft: false
tags: ['Transformation', 'Validation Rules', 'Regular Expressions']
date: 2023-02-23

group: advanced-etl-processor-enterprise-regular-expressions-validation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/is_email_valiadtion_function.png" title="Is Email Validation Function" >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                                                                                             |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Category    | Validation Function                                                                                                                                               |
| Description | Email Address validation that allows both IP addresses and regular domains. In the case of an IP address it makes sure that it is no more than 255 for each part. |
| Properties  | Default                                                                                                                                                           |
| Pass        | john@doe.com                                                                                                                                                      |
| Fail        | john@doe                                                                                                                                                          |

{{< /table >}}

{{< alert color="secondary">}}To change validation function properties double click on it{{< /alert >}}

[Back to Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}
