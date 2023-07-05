---
author: Peter Jonson
title: Interbase/Firebird Connection
description: Interbase/Firebird Database Connection
draft: false
tags: ['Connection', 'Database', 'Interbase', 'Firebird']
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
date: 2023-07-05
layout: docs
---

## About Interbase

InterBase is a relational database management system (RDBMS) currently developed and marketed by Embarcadero Technologies. InterBase is distinguished from other DBMSs by its small footprint, close to zero administration requirements, and multi-generational architecture. InterBase runs on the Linux, Microsoft Windows, Mac OS X and Solaris operating systems.

## About Firebird

Firebird is a relational database offering many ANSI SQL standard features that runs on Linux, Windows, and a variety of Unix platforms. Firebird offers excellent concurrency, high performance, and powerful language support for stored procedures and triggers. It has been used in production systems, under a variety of names, since 1981.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/interbase-connection.png" title="Interbase/Firebird Connection" >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/interbase-connection-comments.png" title="Microsoft SQL Server CE Connection Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/interbase-connection-user-fields.png" title="Microsoft SQL Server CE Connection User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

## Creating Interbase/Firebird connection

- In the Name Text Box type in a new name for the connection you are about to create
- Type in the database name
- Fill in Username/Password for the database you wish to connect to
- Click Test Connection to ensure the details you have provided are correct
- Click OK to close the connection properties window

{{< aetl >}}
