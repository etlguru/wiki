---
author: Maria Salter
title: Working with Greenplum
description: This article describes how to work with Greenplum databases
draft: false
tags: ['Knowledgebase', 'Connection', 'Greenplum', 'PostgreSQL']
date: 2023-03-14
group: knowledgebase-connections
layout: docs
---

**About Greenplum**

The Greenplum Database builds on the foundations of the open source database **PostgreSQL**. It primarily functions as a data warehouse and utilizes a shared-nothing, massively parallel processing (MPP) architecture. In this architecture, data is partitioned across multiple segment servers, and each segment owns and manages a distinct portion of the overall data; there is no disk-level sharing nor data contention among segments.

Source: Wikipedia.

Unlike **PostgreSQL, Greenplum** database does not support the binary option of [copy command](http://www.postgresql.org/docs/8.3/static/sql-copy.html)

Select the Text Mode option to load data into Greenplum

{{< image class="mx-auto d-block"  src="/images/knowledgebase/greenplum.png" title="Greenplum" >}}

{{< aetl >}}
