---
author: Peter Jonson
title: Working with Log Object
description: Log Object allows redirecting log information into different data flow, so the end user can address the data quality issues.
draft: false
tags: ['Transformation', 'Log']
date: 2022-09-17
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

**Log Object** redirects log information into different data flow, so the end user can address the data quality issues.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/log.png" title="Log Object" >}}

Log Object provides more detailed information about data quality than standard log

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/log-transformation.png" title="Log Transformation" >}}

## Output Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/log-validation.png" title="Log Validation" >}}

Log Object answers the following questions:

- What was wrong with the data?
- Which actions were taken to correct the data?
- An initial value of the field
- Value after correction

{{< alert color="secondary">}}Additional information such as user/computer/package name can be extracted using Metadata transformation object
{{< /alert >}}

{{< aetl >}}
