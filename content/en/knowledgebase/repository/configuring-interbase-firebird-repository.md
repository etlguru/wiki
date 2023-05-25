---
author: Maria Salter
title: Configuring Interbase/Firebird Repository
description: This Article describes configuring Interbase/Firebird Repository
draft: false
tags: ['Knowledgebase', 'Interbase', 'Firebird', 'Repository']
date: 2023-03-14
group: knowledgebase-repository
layout: docs
weight: 3
---

The repository database stores all the information about connections, transformations, packages, SQL scripts, reports and execution logging. This is where the results of ETL designer hard work is stored and obviously, no one wants to lose it.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/interbase-firebird.png" title="Configuring Interbase/Firebird Repository" >}}

- [Repository Tables]({{<ref "repository-tables" >}})

{{< alert color="warning" >}}
Although it is possible to use Interbase or Firebird as repository we always recommend using MS SQL Server express. It is free and the easiest option  
{{< /alert >}}

{{< aetl >}}
