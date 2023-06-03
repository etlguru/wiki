---
author: Peter Jonson
title: ODBC Reader
description: ODBC Reader
draft: false
tags: ['Reader', 'ODBC']
date: 2023-01-05
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## ODBC

In computing, Open Database Connectivity (ODBC) is a standard application programming interface (API) for accessing database management systems (DBMS). The designers of ODBC aimed to make it independent of database systems and operating systems. An application written using ODBC can be ported to other platforms, both on the client and server side, with few changes to the data access code.

Source: [Wikipedia](https://en.wikipedia.org/wiki/Open_Database_Connectivity)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/odbc.png" title="ODBC Reader" >}}

## Bulk fetch

Some ODBC drivers do not support bulk fetch.
If table has blob fields use SQL as source and put blob fields last

```sql
Select field1,blob1,blob2 from table
```

## Connection Strings

It also possible to use ODBC connection strings for both Reader and Writer connections.
For example for MS SQL Server connection string is:

```
Driver={SQL Native Client};Server=myServerAddress;Database=myDataBase;Uid=myUsername;Pwd=myPassword;
```

One of the major benefits of using connection strings that it makes it no longer necessary to create ODBC Dsn’s manually on every single computer where [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) is installed. It also gives a greater control over the connection parameters.

Leave user name and password blank and provide it within connection string

More information about connection strings can be found at: https://www.connectionstrings.com

The simplest way to create ODBC connection string is to use ODBC Connection builder dialog. Double click on ODBC driver name to create a connection string

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/odbc-connection-strings.png" title="ODBC Connection builder" >}}

## Data View

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/odbc-data-view.png" title="Data View" >}}

## Data View Toolbar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/odbc-dataview-toolbar.png" title="Data View Toolbar" >}}

1. Reader Properties
1. Refresh Data
1. Browse Data
1. Switch to Data View
1. Switch to Data Definition View

## Data Definition View

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/odbc-data-definition-view.png" title="Data Definition View" >}}

## Data Definition View Toolbar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/odbc-data-definition-toolbar.png" title="Data Definition View Toolbar" >}}

1. Reader Properties
1. Refresh Data
1. Print Data Definition
1. Print Preview Data Definition
1. Find
1. Browse Data
1. Switch to Data View
1. Switch to Data Definition View

[List of ODBC Drivers Download Links]({{<relref "/knowledgebase/tips/list-of-odbc-drivers-download-links" >}})
