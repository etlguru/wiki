---
author: Maria Salter
title: Configuring PostgreSQL Repository
description: This Article describes configuring PostgreSQL Repository
draft: false
tags: ['Knowledgebase', 'PostgreSQL', 'Repository']
date: 2023-03-14
group: knowledgebase-repository
layout: docs
weight: 3
---

The repository database stores all the information about connections, transformations, packages, SQL scripts, reports and execution logging. This is where the results of ETL designer hard work is stored and obviously, no one wants to lose it.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/postgresql-5.png" title="PostgreSQL Connection" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/postgresql-6.png" title="PostgreSQL Connection" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/postgresql-7.png" title="PostgreSQL Connection" >}}
\

- [Repository Tables]({{<ref "repository-tables" >}})

{{< alert color="warning" >}}
Although it is possible to use PostgreSQL as repository we always recommend using MS SQL Server express. It is free and the easiest option  
{{< /alert >}}

{{< aetl >}}
