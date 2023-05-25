---
author: Maria Salter
title: Configuring SQL Server Repository
description: This article provides information about configuring MS SQL Server Repository connection
draft: false
tags: ['Knowledgebase', 'SQL Server', 'Repository']
date: 2023-03-14
group: knowledgebase-repository
layout: docs
weight: 3
---

The repository database stores all the information about connections, transformations, packages, SQL scripts, reports and execution logging. This is where the results of ETL designer hard work is stored and obviously, no one wants to lose it.

## About

This article provides information about configuring MS SQL Server Repository connection

All versions are supported including 2000, 2005, 2008, 2012, 2014, 2017, 2019, 2022 and Compact Edition.

## To create new MS Sql Server repository connection

- Click Options
- Click Plus
- Enter a connection name
- Set type to MS SQL Server
- Select/Enter server name
- Enter username and password
- Select database name
- Make sure that connection actually works

{{< image class="mx-auto d-block"  src="/images/knowledgebase/ms-sql-server-repository-1.png" title="SQL Server Repository" >}}
\
{{< alert color="secondary" >}}When username and password are blank windows authentication is used{{< /alert >}}

## Creating MS Sql Server repository

- Click Options
- Click Plus
- Enter a connection name
- Set type to Ole DB
- Select build connection
- Select relevant Ole DB provider and enter necessary parameters
- Make sure that connection actually works

{{< image class="mx-auto d-block"  src="/images/knowledgebase/ms-sql-server-repository-2.png" title="SQL Server Repository" >}}

To avoid issues with date fields always use English as the default language for repository user

{{< image class="mx-auto d-block"  src="/images/knowledgebase/ms-sql-server-language.png" title="SQL Server Language" >}}
\
{{< alert color="secondary" >}}To avoid problems always make sure that you are using the latest version of 32 or 64 bit MS SQL Server client{{< /alert >}}
\
{{< alert color="secondary" >}}Using SQL Server username and password is always better than using windows authentication.{{< /alert >}}

Consider the following scenario.
Administrator John installs the software everything is working fine.
Developer Peter logs in, nothing is working, because the developer has no access to the repository database.
Peter gets proper access and he can do his job.
Over the weekend another administrator want to check execution status he logs in, the same problem happens again.

## OLE DB Provider

By default, MS SQL Server repository connection is using Microsoft OLE DB Provider for SQL Server, it is possible to use different OLE DB Provider by switching to OLE DB Repository connection type.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/oledb.png" title="OleDB" >}}

- [Repository Tables]({{<ref "repository-tables" >}})
- [Getting latest version of SQL Server ODBC Drivers]({{<ref "getting-latest-version-of-sql-server-odbc-drivers" >}})

{{< aetl >}}
