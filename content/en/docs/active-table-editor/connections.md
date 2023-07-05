---
author: Maria Salter
title: Connections
description: Active Table Editor Connections
draft: false
tags: ['Active Table Editor', 'Data Entry', 'Connections']
date: 2023-07-04
menu: active-table-editor
group: active-table-editor
layout: docs
---

In order to edit the data, [Active Table Editor](https://www.etl-tools.com/active-table-editor/overview.html) must be able to connect to the database.

## Supported Databases/Connections

- Oracle
- MS SQL Server
- Microsoft SQL Server CE
- Interbase or Firebird
- MySQL
- PostgreSQL
- SQLite
- Ole DB
- ODBC

## Toolbar

{{< image class="mx-auto d-block"  src="/images/active-table-editor/connections-toolbar.png" title="Connections toolbar" >}}

1. Properties
1. Refresh list
1. Add connection
1. Delete connection
1. Clone connection
1. Print
1. Print preview
1. Find
1. Enable Incremental search
1. Show grouping panel
1. Export grid
1. Export data to excel
1. Customize columns
1. Auto format grid

## Creating New Connections

To create a **New Connection**, Click **Outlook Bar**-> **Management**-> **Connections**->**Plus Icon**
\
{{< image class="mx-auto d-block"  src="/images/active-table-editor/connections-new-connections.png" title="New connection" >}}

1. Dialog box will appear.
2. Select the appropriate connection type
3. In the Name Text Box type in a new name for the connection you are about to create
4. Fill in server name/database name/port number and all other relevant information
5. Fill in Username/Password
6. Click Test to ensure the details you have provided are correct

{{< alert color="secondary" >}}
**Note:** To refresh the list of databases double click on it
{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/active-table-editor/connections-odbc-con-properties.png" title="ODBC Connection Properties" >}}

## ODBC Connection Strings

It also possible to use ODBC connection strings for both Reader and Writer connections.

For example for MS SQL Server connection string is:
Driver={SQL Native Client};
Server=myServerAddress;Database=myDataBase;Uid=myUsername;Pwd=myPassword;

One of the major benefits of using connection strings that it makes it no longer necessary to create ODBC Dsn’s manually on every single computer where Advanced ETL Processor is installed. It also gives a greater control over the connection parameters.

{{< alert color="secondary" >}}
**Note:** Leave username and password blank and provide it within the connection string
{{< /alert >}}

More information about connection strings can be found at: https://www.connectionstrings.com

The simplest way to create ODBC connection string is to use ODBC Connection builder dialogue. Double click on ODBC driver name to create a connection string.

{{< image class="mx-auto d-block"  src="/images/active-table-editor/connections-odbc-connection-builder.png" title="ODBC connection builder" >}}

## Table Browser

Allows editing data in tables, run scripts or create/drop database objects.

{{< image class="mx-auto d-block"  src="/images/active-table-editor/connections-table-browser.png" title="Table Browser" >}}

{{< ate >}}
