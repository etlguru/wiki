---
author: Maria Salter
title: Repository
description: Active Table Editor Repository Database
draft: false
tags: ['Active Table Editor', 'Data Entry', 'Repository']
date: 2022-09-17
menu: active-table-editor
group: active-table-editor
layout: docs
---

All objects are stored in the repository, the default repository database type is Microsoft Access.

## Supported repository types

- MS Access
- SQL Server
- Oracle
- PostgreSOL
- MySQL
- Interbase/Firebird

{{< alert color="danger" >}}
It is not recommended to use MS Access as a repository in the production environment,\
it tends to get corrupted over time
{{< /alert >}}

## Creating new repository

- Log in as an Administrator
- Click Tools => Run Repository Creation Wizard
- Follow The Wizard steps
- Connect to the newly created repository

The repository creation scripts located in:

C:\Users\Public\Documents\DBSL\Repository Scripts\Repository

- [Repository Tables]({{<ref "/knowledgebase/repository/repository-tables" >}})
- [Configuring SQL Server Repository]({{<ref "/knowledgebase/repository/configuring-sql-server-repository" >}})
- [Configuring Interbase/Firebird Repository]({{<ref "/knowledgebase/repository/configuring-interbase-firebird-repository" >}})
- [Configuring MySQL Repository]({{<ref "/knowledgebase/repository/configuring-mysql-repository" >}})
- [Configuring PostgreSQL Repository]({{<ref "/knowledgebase/repository/configuring-postgresql-repository" >}})

{{< ate >}}
