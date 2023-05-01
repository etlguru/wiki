---
author: Peter Jonson
title: MS SQL Server Reader
description: MS SQL Server Reader
draft: false
tags: ['Reader', 'SQL Server']
date: 2023-03-08
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/ms-sql-server.png" title="MS SQL Server" >}}

- All properties are very similar to ODBC connection
- Leave user name and password blank to use Windows Authentication
- To connect using different port use "server name,port" format

**ODBC Drivers**

Our software automatically selects the highest installed driver in the following order

- ODBC Driver 17 for SQL Server
- ODBC Driver 13 for SQL Server
- ODBC Driver 11 for SQL Server
- SQL Server Native Client 11.0
- SQL Server Native Client 10.0
- SQL Native Client
- SQL Server

{{< alert color="secondary">}}
Always Use set sql nocount on inside Microsoft SQL Server Stored Procedures, Triggers and Scripts
{{< /alert >}}

- [Getting latest version of SQL Server ODBC Drivers]({{<relref "/knowledgebase/tips/getting-latest-version-of-sql-server-odbc-drivers" >}})
