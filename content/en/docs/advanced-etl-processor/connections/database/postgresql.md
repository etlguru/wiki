---
author: Peter Jonson
title: PostgreSQL Connection
description: PostgreSQL Database Connection
draft: false
tags: ['Connection', 'Database', 'PostgreSQL']
date: 2023-07-05
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

## About PostgreSQL

PostgreSQL is a powerful, open-source object-relational database system. It has more than 15 years of active development and a proven architecture that has earned it a strong reputation for reliability, data integrity, and correctness. It runs on all major operating systems, including Linux, UNIX (AIX, BSD, HP-UX, SGI IRIX, Mac OS X, Solaris, Tru64), and Windows. It is fully ACID compliant, and has full support for foreign keys, joins, views, triggers, and stored procedures (in multiple languages). It includes most SQL:2008 data types, including INTEGER, NUMERIC, BOOLEAN, CHAR, VARCHAR, DATE, INTERVAL, and TIMESTAMP. It also supports the storage of large binary objects, including pictures, sounds, or videos.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/postgresql.png" title="Creating PostgreSQL connection" >}}
\
{{< alert color="secondary" >}}
There are three ways of connecting to PostgreSQL: Direct, Via SSL and Via SSH
{{< /alert >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/postgresql1.png" title="Creating PostgreSQL connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/postgresql2.png" title="Creating PostgreSQL connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/postgresql3.png" title="Creating PostgreSQL connection" >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/postgresql-connection-comments.png" title="PostgreSQL Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/postgresql-connection-user-fields.png" title="PostgreSQL User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

## Creating New Connection

- In the Name Text Box type in a new name for the connection you are about to create
- Type in the hostname
- Select a Database name from the drop-down List
- Select appropriate connection port default is 5432
- Fill in the Username/Password for the database you wish to connect to
- Fill in SSL/SSH connection details if necessary
- Click Test Connection to ensure the details you have provided are correct
- Click OK to close the connection properties window

[Working with Greenplum]({{<relref "/knowledgebase/connections/working-with-greenplum" >}})

{{< aetl >}}
