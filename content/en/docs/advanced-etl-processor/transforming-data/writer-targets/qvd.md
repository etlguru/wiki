---
author: Peter Jonson
title: QVD Writer
description: QVD Writer
draft: false
tags: ['Writer', 'QVD', 'Qlik', 'QlikView', 'QlikSense']
date: 2022-09-17
group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

A QlikView QVD file holds exactly one data table and consists of three parts:

- A well-formed XML header (in UTF-8 char set) describing the fields in the table, the layout of the subsequent information and some other meta-data.
- Symbol tables in a byte stuffed format.
- Actual table data in a bit-stuffed format.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/qvd.png" title="QVD" >}}

**Note:**

Use data writer definition grid to change field’s types.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/qvd-definition.png" title="QVD Writer Definition" >}}

{{< aetl >}}
