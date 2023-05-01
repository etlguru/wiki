---
author: Peter Jonson
title: Editions
description: Advanced ETL Processor Editions
draft: false
tags: ['Editions']
date: 2022-08-01
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
weight: 1000
layout: docs
---

There are three editions of [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)

## Standard Edition

This edition supports data transformations only. Data transformations as stored as files. Standard Edition is usually recommended to occasional users

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/introduction/advanced-etl-processor-standard.png" title="Advanced ETL Processor Standard" >}}

## Professional Edition

This edition supports designing both data transformations and automation packages, it is usually recommended for developers.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/introduction/advanced-etl-processor-enterprise.png" title="Advanced ETL Processor Enterprise" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/introduction/advanced-etl-processor-enterprise-package.png" title="Advanced ETL Processor Enterprise Services" >}}

## Enterprise Edition

On top of the above this edition has multiple windows services which are used for automated execution, Enterprise Edition is recommended for running on the servers

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/introduction/advanced-etl-processor-enterprise-services.png" title="Advanced ETL Processor Enterprise Services" >}}

## Repository

Both Professional and Enterprise Editions are use [repository]({{<relref "docs/advanced-etl-processor/repository-database" >}}) database to store data. The repository database structure is the same for both editions. Multiple users of our ETL software can connect to the same repository and share the data

{{< aetl >}}
