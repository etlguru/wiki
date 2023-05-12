---
author: Peter Jonson
title: Demo Data
description: Advanced ETL Processor Demo Data
draft: false
tags: ['Demo Data', 'Introduction']
date: 2022-08-01
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
weight: 4000
layout: docs
---

In order to provide a flavor of the types of data the [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) can handle, a number of different file types have been provided for demonstration purposes.

A range of different types of data files have been provided, in addition to SQL scripts to create database tables in Oracle, and MS SQL Server.

## Text files

Examples provided are using text files in

{{< command >}}
C:\Users\Public\Documents\DBSL\Demo\Buffer and\
C:\Users\Public\Documents\DBSL\Demo\Text Files
{{< /command >}}

## Access Databases

{{< command >}}
C:\Users\Public\Documents\DBSL\Demo\MS Access
{{< /command >}}

## DBF Files

{{< command >}}
C:\Users\Public\Documents\DBSL\Demo\DBF
{{< /command >}}

## Excel Files

{{< command >}}
C:\Users\Public\Documents\DBSL\Demo\Excel
{{< /command >}}

{{< alert color="secondary">}}
If you want to use other locations please amend Directories properties.
{{< /alert >}}

## Demo Tables

Use SQL Scripts provided to create demo tables for Oracle and MS SQL Server.
Please adjust connection details before executing these scripts.

Most of the SQL Server Imports use DEMO database. You have to create demo tables within this database first before executing import scripts.

## ODBC connections

During the setup process, the following ODBC DSN is created during the installation:

- ODBC_FOXPRO
- ODBC_ACCESS_SOURCE
- ODBC_ACCESS_TARGET
- ODBC_MS
- ODBC_ORACLE
- ODBC_EXCEL

These ODBC connections provide the basis for the ETL Processor to perform its tasks and process different types of data, while ensuring that the automation of these processes is completely transparent.

{{< aetl >}}
