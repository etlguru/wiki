---
author: Peter Jonson
title: ODBC Connections
description: ODBC Database Connection
draft: false
tags: ['Connection', 'Database', 'ODBC']
date: 2023-03-22
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

## ODBC history

ODBC, standing for Open DataBase Connectivity, represents a standard database access method working as SQL API software. It was developed back in 1992 with the sole purpose of facilitating the work with database management systems (DBMS). It was created by the Microsoft Corporation and is since then included in every copy of Microsoft Windows. In 1995 the ODBC was included in the SQL Standard, which played a great role in making ODBC more popular. Today, there are versions for almost any operating system currently used.

## How ODBC works

ODBC was intended to enable developers' access to any data through any application, regardless of the DBMS used for managing that data. ODBC boasts platform independence since it has been purposefully designed in a way that makes it distinct from database systems, programming languages and operating systems.

Facilitating the data access from an application to a database management system through ODBC is done through a specific mechanism. A common ODBC implementation contains one or more applications, a core ODBC 'Driver Manager' library, and one or more database drivers. The Driver Manager's role is to interpret the data queries coming from an application by using the DBMS-specific details contained in database drivers. The latter represents a middle layer inserted between an application and the DBMS in use. This way, the application's data queries are translated into commands that can easily be read by the DBMS.

A basic requirement for an ODBC implementation to be run is that both the application and the DBMS be ODBC-compliant. In other words, the application must be able to issue ODBC commands and the DBMS must be capable of responding to them.

Thanks to its modular nature ODBC gives developers great freedom in creating the separate components of an ODBC implementation. Thus, a programmer can write applications that use standard features without needing to worry about the type of DBMS used for administering the database that the application tries to access. Likewise, the only thing the database driver programmers need to keep in mind during the development process is how to attach their database driver to the 'Driver Manager' library. The result is that currently there are hundreds of ODBC drivers created for a large variety of data sources.

Thanks to the long period of existence and the fruitful efforts of its team of developers, ODBC now offers access to a much wider range of data sources than any other database access method available today. It has turned into a universal data access standard, working with a great variety of operating systems and providing access to even non-relational data, including text and XML files.

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/odbc-drivers-list.png" title="ODBC drivers list" >}}
\
{{< alert color="secondary">}}The ODBC Connection properties dialogue allows the administrator to create appropriate connections to various databases. It is necessary to create connections to databases, whenever they are to be processed.{{< /alert >}}

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/odbc.png" title="ODBC" >}}

## Creating New Connection

- In the Name Text Box type in a new name for the connection you are about to create
- Select an ODBC DSN Name from Server Drop Down List
- Fill in Username/Password for the database you wish to connect to
- Click Test to ensure the details you have provided are correct
- Click OK to close the connection properties window

You may use ODBC admin to create/modify ODBC data sources.
Some drivers do not support Unicode use ANSI Driver checkbox for these situations
The 32-bit edition of our software uses 32-bit drivers and the 64-bit edition uses 64-bit drivers

## ODBC Connection Strings

It also possible to use ODBC connection strings for both Reader and Writer connections.
For example for MS SQL Server connection string is:

```
Driver={SQL Native Client};Server=myServerAddress;Database=myDataBase;Uid=myUsername;Pwd=myPassword;
```

One of the major benefits of using connection strings that it makes it no longer necessary to create ODBC Dsn’s manually on every single computer where Visual Importer ETL is installed. It also gives a greater control over the connection parameters.

Leave Username and password blank and provide them within the connection string

More information about connection strings can be found at: https://www.connectionstrings.com

The simplest way to create an ODBC connection string is to use the ODBC Connection builder dialogue. Double click on the ODBC driver name to create a connection string

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/odbc-connections-builder.png" title="ODBC Connection Builder" >}}
\
[List of ODBC Drivers Download Links]({{<relref "/knowledgebase/tips/list-of-odbc-drivers-download-links" >}})
