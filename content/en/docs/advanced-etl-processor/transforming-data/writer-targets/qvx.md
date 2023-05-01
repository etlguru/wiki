---
author: Peter Jonson
title: QVX Writer
description: QVX Writer
draft: false
tags: ['Writer', 'Qvx', 'Qlik', 'QlikView', 'QlikSense']
date: 2022-09-17
group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

**QVX** (QlikView data eXchange) is a new file/stream format for high performance data input into QlikView. A QVX formatted file contains metadata describing a table of data and the actual data. In contrast to the QVD format, which is proprietary and optimized for minimum transformations inside QlikView, the QVX format is public and requires a few transformations when exporting data from traditional data base formats.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/qvx.png" title="QVX" >}}

**Note:**

To create date fields use standard Date Format function

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/date_format_transformation_function.png" title="QVX Date Format" >}}

{{< aetl >}}
