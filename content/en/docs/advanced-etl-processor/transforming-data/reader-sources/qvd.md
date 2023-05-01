---
author: Peter Jonson
title: QVD Reader
description: QVD Reader
draft: false
tags: ['Reader', 'QVD']
date: 2023-01-05
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About QVD Files

A QlikView QVD file holds exactly one data table and consists of three parts:

- A well-formed XML header (in UTF-8 charset) describing the fields in the table, the layout of the subsequent information - and some other meta-data.
- Symbol tables in a byte stuffed format.
- Actual table data in a bit-stuffed format.

A QVD contains the physical representation of an in-memory QlikView Table.
This “RAM image” format is what allows an optimized QVD load to be so quick. The physical blocks of the disk are read directly into RAM, “ready to go”.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/qvd.png" title="QVD Reader" >}}

## Avoiding Problems with numeric fields

Numeric fields can be represented as a number or as a date (or timestamp).
The software is trying to guess the data type and in certain situations, it is not possible to do it correctly.
Ignore format option forces numeric representation of the data.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/qvd-ignore-format-1.png" title="QVD Reader" >}}
/
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/qvd-ignore-format-2.png" title="QVD Reader" >}}

## Video Tutorial

{{< youtube id="pqfj51oGZG4" class="ratio ratio-16x9" >}}
