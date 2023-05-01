---
author: Peter Jonson
title: Microsoft SQL Server Connection
description: Microsoft SQL Server Database Connection
draft: false
tags: ['Connection', 'Database', 'SQL Server']
date: 2022-08-01
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

The procedure for many database connections is very similar. In the case of MS SQL Server, it is necessary to specify the server, database name and user name/password combination.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/ms-sql-server.png" title="Microsoft SQL Server Connection" >}}

## Creating New Connection

- In the Name Text Box type in a new name for the connection you are about to create
- Select a Server Name from Server Drop Down List
- Select a Database Name from the Drop Down List
- Fill in Username/Password for the database you wish to connect to
- Click Test to ensure the details you have provided are correct
- Click OK to close the connection properties window

Leave user name and password blank to use Windows Authentication
To connect using different port use "server name,port" format

{{< alert color="secondary" >}}
If you are unsure of these parameters, please contact your Database Administrator for the correct settings.
{{< /alert >}}

## ODBC Drivers

Our software automatically selects the highest installed driver in the following order

- ODBC Driver 17 for SQL Server
- ODBC Driver 13 for SQL Server
- ODBC Driver 11 for SQL Server
- SQL Server Native Client 11.0
- SQL Server Native Client 10.0
- SQL Native Client
- SQL Server

## Video Tutorial

{{< youtube id="EN1CtjAHGCA" class="ratio ratio-16x9" >}}
