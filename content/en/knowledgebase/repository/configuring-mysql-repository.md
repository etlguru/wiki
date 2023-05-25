---
author: Maria Salter
title: Configuring MySQL Repository
description: This Article describes configuring MySQL Repository
draft: false
tags: ['Knowledgebase', 'MySQL', 'MariaDB', 'Repository']
date: 2023-03-14
group: knowledgebase-repository
layout: docs
weight: 3
---

The repository database stores all the information about connections, transformations, packages, SQL scripts, reports and execution logging. This is where the results of ETL designer hard work is stored and obviously, no one wants to lose it.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/mysql.png" title="Database" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/metadata.png" title="Metadata" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/cursor.png" title="Cursor" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/debug.png" title="Debug" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/ssl.png" title="SSL" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/misc.png" title="Misc" >}}

It is recommended to increase max_allowed_packet.
The server's default max_allowed_packet value is 1MB.
You can increase this if the server needs to handle big queries
(for example, if you are working with big BLOB columns).
For example, to set the variable to 16MB, start the server like this:
shell> mysqld --max_allowed_packet=16M
You can also use an option file to set max_allowed_packet.
For example, to set the size for the server to 16MB, add the following lines in an option file:
[mysqld] max_allowed_packet=16M

- [Repository Tables]({{<ref "repository-tables" >}})

{{< alert color="warning" >}}
Although it is possible to use MySQL or MariaDB as repository we always recommend using MS SQL Server express. It is free and the easiest option  
{{< /alert >}}

{{< aetl >}}
