---
author: Peter Jonson
title: Requirements
description: Requirements for Advanced ETL Processor
draft: false
tags: ['Requirements']
date: 2022-12-22
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
weight: 2000
layout: docs
---

Our ETL software works on Windows only.

## Software Requirements

Below is a List of Software that must be installed before installation of [ETL Software](https://www.etl-tools.com):

{{< table "table-striped table-bordered" >}}

| Software                       | Version                   |                    | Notes                                             |
| ------------------------------ | ------------------------- | ------------------ | ------------------------------------------------- |
| Microsoft Windows XP or higher |                           |                    |
| FoxPro ODBC driver             | 6.1.8629.1 or higher      | Separate download  | Only to work with DBF/FoxPro Files                |
| SQL ODBC driver                | 2000.81.9041.40 or higher | Part of OS         | Only to import data into MS SQL Server 2008/2019  |
| Interbase client               |                           | GDS32.DLL          | Only to work with Interbase or Firebird Databases |
| Oracle Client                  | 7.3.4 or higher           | Provided by Oracle | Only to work with Oracle Databases                |
| SQLite                         |                           | Sqlite3.dll        | Only to work with SQLite databases                |
| BDE Drivers                    | Latest Version            |                    | Only to work with Paradox or other BDE databases  |
| Tableau Client                 | Latest Version            |                    | Only to work with Tableau                         |

{{< /table >}}

## Separate Downloads:

### FoxPro ODBC driver

https://github.com/VFPX/VFP9SP2Hotfix3/blob/master/ODBC_Release_Notes.md

### FoxPro OleDB provider

https://github.com/VFPX/VFP9SP2Hotfix3/blob/master/OLEDB_Release_Notes.md

### Office 2010 Data Access Components

https://www.microsoft.com/en-gb/download/details.aspx?id=13255

### BDE

https://www.etl-tools.com/dmdocuments/BDE.zip

### Python

https://www.python.org/downloads/

## Working with Oracle

{{< alert color="secondary">}}
Oracle client 8.1.7 to load data into/from Oracle\
Or\
Oracle client 9 to load data into/from Oracle\
Or\
Oracle client 10 to load data into/from Oracle\
Or\
Oracle client 11 to load data into/from Oracle\
Or\
Oracle client 12 to load data into/from Oracle\
Or\
Oracle client 18 to load data into/from Oracle
{{< /alert >}}

## Working with SQL Server

- [Getting latest version of SQL Server ODBC Drivers]({{<relref "/knowledgebase/tips/getting-latest-version-of-sql-server-odbc-drivers" >}})

## Using ODBC

- [List of ODBC Drivers Download Links]({{<relref "/knowledgebase/tips/list-of-odbc-drivers-download-links" >}})

{{< alert color="secondary">}}
Depending on the Requirements you may or may not need to have all components installed. \
There is no need to install clients for MySql and PostgreSQL they are integrated into the software itself
{{< /alert >}}

## Hardware recommendationss

The installation may use up to 120 meg of disk space.
We recommend using 8 gigabytes of memory.
Our software streams data, therefore, having loads of memory is not going to improve performance.
(eg: it does not load all the data into memory at once).
Repository database takes approximately 200 megs.

We do have customers running our ETL software on low-end servers in the cloud.

Most of the time two i7 processors and 16 gigs of memory is more than enough.
We prefer not to force someone to buy expensive hardware which is not going to be used.
It is better to start small and upgrade later.

{{< aetl >}}
