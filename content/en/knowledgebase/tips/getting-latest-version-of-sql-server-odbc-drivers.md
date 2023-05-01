---
author: Maria Salter
title: Getting latest version of SQL Server ODBC Drivers
description: Getting latest version of SQL Server ODBC Drivers
draft: false
tags: ['Knowledgebase', 'SQL Server', 'ODBC']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## Important Note

- 32-bit applications use 32-bit ODBC drivers
- 64-bit applications use 64-bit ODBC drivers

{{< alert color="secondary" >}}Our software uses the highest driver installed,
For example, If both SQL server 2016 and 2017 drivers are installed it will use SQL Server 2017 Driver.{{< /alert >}}

To Check Version of SQL Server ODBC Driver do the following

- Click Maintain
- Click ODBC Manager

{{< image class="mx-auto d-block"  src="/images/knowledgebase/odbc-sql-server.png" title="ODBC" >}}

## Here are the links to the latest version of SQL Server ODBC drivers:

### Feature Pack for Microsoft SQL Server 2008

[Download Driver](https://www.microsoft.com/en-gb/download/details.aspx?id=44277)

**Download Instructions**

- Hit the Download button.
- Check ENU\x86\sqlncli.msi for the 32-bit version installation package
- Or Check ENU\x64\sqlncli.msi for the 64-bit version installation package
- Click Next.
- Download Starts.

### Feature Pack for Microsoft SQL Server 2008 R2

[Download Driver](https://www.microsoft.com/en-us/download/details.aspx?id=44272)

**Download Instructions**

- Hit the Download button.
- Check ENU\x86\sqlncli.msi for the 32-bit version installation package
- Or Check ENU\x64\sqlncli.msi for the 64-bit version installation package
- Click Next.
- Download Starts.

### Feature Pack for Microsoft SQL Server 2012

[Download Driver](https://www.microsoft.com/en-us/download/details.aspx?id=56041)

**Download Instructions**

- Hit the Download button.
- Check ENU\x86\sqlncli.msi for the 32-bit version installation package
- Or Check ENU\x64\sqlncli.msi for the 64-bit version installation package
- Click Next.
- Download Starts.

### Feature Pack for Microsoft SQL Server 2016

[Download Driver](https://www.microsoft.com/en-us/download/details.aspx?id=56833)

**Download Instructions**

- Hit the Download button.
- Check ENU\x86\sqlncli.msi for the 32-bit version installation package
- Or Check ENU\x64\sqlncli.msi for the 64-bit version installation package
- Click Next.
- Download Starts.

### Feature Pack for Microsoft SQL Server 2017

[Download Driver](https://www.microsoft.com/en-us/download/details.aspx?id=55992)

**Download Instructions**

- Hit the Download button.
- Check ENU\x86\sqlncli.msi for the 32-bit version installation package
- Or Check ENU\x64\sqlncli.msi for the 64-bit version installation package
- Click Next.
- Download Starts.

### ODBC Driver 17 and 18

[Download Driver](https://docs.microsoft.com/en-us/sql/connect/odbc/download-odbc-driver-for-sql-server?view=sql-server-ver15)

{{< alert color="secondary" >}}Use SQL Server 2012 Drivers for SQL Server 2014{{< /alert >}}

{{< alert color="secondary" >}}Most of the time existing drivers work fine with all versions of SQL Server all you need to do is to make sure that you have the latest driver installed, so if you have SQL server 2008 driver installed and work with SQL server 2012 make sure that you have the latest version of SQL server 2008 driver installed {{< /alert >}}

{{< aetl >}}
