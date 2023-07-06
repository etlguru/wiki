---
author: Peter Jonson
title: BDE Connection
description: BDE Database Connection
draft: false
tags: ['Connection', 'Database', 'BDE']
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
date: 2023-07-05
layout: docs
---

## About BDE

Borland Database Engine (BDE) is the Windows-based core database engine and connectivity software behind Borland Delphi, C++Builder, IntraBuilder, Paradox for Windows, and Visual dBASE for Windows.

## History

Borland’s Turbo Pascal included a "database" Toolbox, it was the beginning of the Borland compiler add-ons that facilitated database connectivity. Then came the Paradox Engine for Windows – PXENGWIN – which could be compiled into a program to facilitate connectivity to Paradox tables.

The first DLL-based connectivity engine was ODAPI (Open Database API). It represented Borland’s attempt to centralise connectivity in its suite of applications which included the brand-new Paradox for Windows 4 and Quattro. With version 4.5 / 5.0 of Paradox for Windows, this database engine was crystallised as IDAPI.

The included set of database drivers enables consistent access to standard data sources: Paradox, dBASE, FoxPro, Access, and text databases. You can add Microsoft ODBC drivers as needed to the built-in ODBC socket. Optionally, Borland's SQL Links product provides access to a range of database management systems (DBMS), including Informix, DB2, InterBase, Oracle, and Sybase.

BDE is object-oriented in design. At runtime, application developers interact with BDE by creating various BDE objects. These runtime objects are then used to manipulate database entities, such as tables and queries. BDE's application program interface (API) provides direct C and C++ optimized access to the database engine, as well as BDE's built-in drivers for dBASE, Paradox, FoxPro, Access, and text databases.

The core database engine files consist of a set of DLLs that are fully re-entrant and thread-safe. Included with BDE are a set of supplemental tools and examples with sample code.

BDE system is configured using the BDE Administrator (BDEADMIN.EXE).

Included with BDE is Borland's Local SQL, a subset of ANSI-92 SQL enhanced to support Paradox and dBASE (standard) naming conventions for tables and fields (called "columns" in SQL). Local SQL lets you use SQL to query "local" standard database tables that do not reside on a database server as well as "remote" DBMS servers. Local SQL is also essential to make multi-table queries across both local standard tables and those on remote SQL servers.

The older name for the BDE API is the "Integrated Database Application Program Interface" or "IDAPI".

Source: Wikipedia

## Recommended settings for BDE

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/bde-administrator.png" title="Recommended settings for BDE" >}}
\
{{< alert color="secondary">}}Although it is possible to work with industrial data bases like Oracle or SQL server using BDE it is not recommended.
BDE is no longer supported by Embacadero.{{< /alert >}}

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/bde-connection.png" title="Creating a BDE connection" >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/bde-connection-comments.png" title="BDE Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/bde-connection-user-fields.png" title="BDE User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

## Creating a BDE connection

- In the Name Text Box type in a new name for the BDE connection you are about to create
- Select appropriate driver
- Fill in connection parameters
- Click OK to close the connection properties window

BDE Connection only works with 32 bit software

## BDE Download

https://www.etl-tools.com/dmdocuments/BDE.zip

{{< aetl >}}
