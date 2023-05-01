---
author: Peter Jonson
title: Editions
description: Visual Importer ETL Editions
draft: false
tags: ['Editions']
date: 2022-08-01
group: visual-importer-etl-enterprise
menu: visual-importer-etl-enterprise
weight: 1000
layout: docs
---

There are three editions of [Visual Importer ETL](https://www.etl-tools.com/visual-importer-etl-standart/overview.html)

## Standard Edition

This edition supports data imports only. Data imports as stored as files. Standard Edition is usually recommended to occasional users

{{< image class="mx-auto d-block"  src="/images/etl/visual-importer-etl/visual-importer-etl-standard.png" title="Visual Importer ETL Standard" >}}

## Professional Edition

This edition supports designing both data imports and automation packages, it is usually recommended for developers.

{{< image class="mx-auto d-block"  src="/images/etl/visual-importer-etl/visual-importer-etl-professional.png" title="Visual Importer ETL Professional" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/visual-importer-etl/visual-importer-etl-enterprise-package.png" title="Visual Importer ETL Enterprise Package" >}}

## Enterprise Edition

On top of the above this edition has multiple windows services which are used for automated execution, Enterprise Edition is recommended for running on the servers

{{< image class="mx-auto d-block"  src="/images/etl/visual-importer-etl/visual-importer-etl-enterprise-services.png" title="Visual Importer ETL Enterprise Services" >}}

## Repository

Both Professional and Enterprise Editions are use [repository]({{<relref "docs/advanced-etl-processor/repository-database" >}}) database to store data. The repository database structure is the same for both editions. Multiple users of our ETL software can connect to the same repository and share the data

{{< alert color="danger" >}}
**Visual importer ETL** is the first ETL software product we created.
Since then we have designed **[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)** which is fully compatible with it and has much more features.\
For all new users we recommend **[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)**
{{< /alert >}}

{{< vimpe >}}
