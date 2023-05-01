---
author: Peter Jonson
title: IP Location
description: IP Location Transformation function returns location attributes of IP address, requires access to the internet, uses cache
draft: false
tags: ['Transformation', 'Transformation Functions', 'Miscellaneous']
date: 2023-03-23

group: advanced-etl-processor-enterprise-miscellaneous-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/ip_location_transformation_function.png" title="IP Location Transformation function" >}}
\
{{< alert color="warning">}}IP Location is a very heavy transformation, it is recommended to create a separate results file and reuse it{{< /alert >}}
\
{{< table "table-striped table-bordered" >}}

| Key         | Value                                                                                  |
| ----------- | -------------------------------------------------------------------------------------- |
| Category    | Transformation Function                                                                |
| Description | Returns Location attributes of IP address, requires access to the internet, uses cache |
| Properties  |                                                                                        |

{{< /table >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/ip_location_properties.png" title="IP Location Transformation function properties" >}}
\
{{< alert color="secondary">}}To change Transformation function properties double click on it{{< /alert >}}

- Register at https://ipstack.com/product to get access key

[Back to Working with Transformer]({{<relref "docs/advanced-etl-processor/transforming-data/transformer" >}})

{{< aetl >}}
