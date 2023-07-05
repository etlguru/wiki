---
author: Peter Jonson
title: OleDB Connection
description: OleDB Database Connection
draft: false
tags: ['Connection', 'Database', 'OleDB']
date: 2023-07-05
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

## About Ole DB

OLE DB (Object Linking and Embedding, Database, sometimes written as OLEDB or OLE-DB) is an API designed by Microsoft for accessing different types of data stored in a uniform manner. It is a set of interfaces implemented using the Component Object Model (COM); it is otherwise unrelated to OLE. It was designed as a higher-level replacement for, and successor to, ODBC, extending its feature set to support a wider variety of non-relational databases, such as object databases and spreadsheets that do not necessarily implement SQL.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/oledb.png" title="Creating Ole DB connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/oledb-connection.png" title="Creating Ole DB connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/oledb-connection1.png" title="Creating Ole DB connection" >}}

## Creating New Ole DB connection

- In the Name Text Box type in a new name for the connection you are about to create
- Type in the connection string or use Build Connection String button to create one.
- Click OK to close the connection properties window

Ole DB is one of the slowest ways of accessing the data and it uses a lot of memory.
It is not recommended for very large datasets.

{{< alert color="secondary">}}Tip: Use variable to connect to the repository{{< /alert >}}

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/repository-connection.png" title="Use variable to connect to the repository" >}}

{{< aetl >}}
