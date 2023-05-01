---
author: Peter Jonson
title: Repository Database
description: The repository database is where our ETL Software users work is stored.
draft: false
tags: ['Repository Database', 'Repository']
date: 2023-01-12
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

The repository database is where our [ETL Software](https://www.etl-tools.com) users work is stored. The default repository database type is MS Access.

{{< alert color="warning" >}}
It is not recommended to use MS Access as a repository in a production environment, it tends to get corrupted over time
{{< /alert >}}

Supported repository types are:

- MS Access
- SQL Server
- Oracle
- PostgreSQL
- MySQL
- Interbase/Firebird

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/maintenance.png" title="Maintenance Tab" >}}
\
{{< alert color="warning" >}}
The repository must be created first
{{< /alert >}}

## Creating new repository

- Click create new
- Follow the Repository creation wizard steps
- Connect to the newly created repository

## Transferring data between repositories

- Connect to a source repository
- Backup repository
- Connect to a target repository
- Restore repository

## Repository objects synchronization

- Run Repository Synchronization Wizard
- Select source repository or repository backup
- Select the target repository
- Drug and drop source repository objects on top of target repository objects to update target object
- Drug and drop source repository objects in the target category to add a new object
- Connect to the target repository and update connections if necessary

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-1.png" title="Repository Synchronization Wizard" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-2.png" title="Repository Synchronization Wizard" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-3.png" title="Repository Synchronization Wizard" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-4.png" title="Repository Synchronization Wizard" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-5.png" title="Repository Synchronization Wizard" >}}

## Knowledgebase Articles

- [Repository Tables]({{<relref "/knowledgebase/repository/repository-tables" >}})
- [Configuring SQL Server Repository]({{<relref "/knowledgebase/repository/repository-tables" >}})
- [Configuring Interbase/Firebird Repository]({{<relref "/knowledgebase/repository/configuring-interbase-firebird-repository" >}})
- [Configuring MySQL Repository]({{<relref "/knowledgebase/repository/configuring-mysql-repository" >}})
- [Configuring PostgreSQL Repository]({{<relref "/knowledgebase/repository/configuring-postgresql-repository" >}})

## Video Tutorials

{{< youtube id="6lRcz7NsU0w" class="ratio ratio-16x9" >}}
\
{{< youtube id="iYFj0d5-Jmw" class="ratio ratio-16x9" >}}
\
{{< youtube id="KgP-TKBsvDc" class="ratio ratio-16x9" >}}
\
{{< youtube id="Kb1rFoh9hng" class="ratio ratio-16x9" >}}

{{< aetl >}}
