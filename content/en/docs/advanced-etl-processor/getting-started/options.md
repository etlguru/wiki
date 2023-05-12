---
author: Peter Jonson
title: Options
description: Advanced ETL Processor Options
draft: false
tags: ['Options']
date: 2023-01-15
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
weight: 5000
layout: docs
---

To access the options dialogue, click System Menu-> File-> Options.

## Repository Tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/repository-options.png" title="Repository Options" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/connection-options.png" title="Connection Options" >}}
\
The Repository tab defines the repository connection. The repository database stores all the information about connections, transformations, packages, SQL scripts, reports and execution logging. This is where the results of the ETL designer's hard work are stored.

The Repository type can be:

- MS Access
- MS SQL Server
- Oracle
- Interbase (Firebird)
- MySql
- PostgreSQL
- ODBC Connection
- OLEDB

{{< alert color="secondary" >}}
Use the Repository creation wizard to create a new repository.
{{< /alert >}}

- [More information about repository database]({{<relref "docs/advanced-etl-processor/repository-database" >}})

## Execution Tab

The execution tab defines settings related to the logging and Packages execution.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/options-execution.png" title="Execution Tab" >}}

## Interface Tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/options-interface.png" title="Interface Tab" >}}

## Email Tab

The Email tab defines default Emails settings.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/options-email.png" title="Email Tab" >}}

## Notifications Tab

The Notifications tab defines Email connection settings for Agent failures and Package notifications.

If enabled

- The agent will send notifications on repository connection failures
- Notifications about execution failures will be sent as well (Packages, Transformations, Imports and SQL scripts)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/options-notifications.png" title="Notifications Tab" >}}

### Email Message Example

Error Message: Reconnected!\
Computer Name: COMPUTER\
User Name: dbsl\
Os Version: Windows 8.1 (Version 6.3, Build 9600, 64-bit Edition)\
Number Of Threads: 11\
Repository: MS SQL Server Repository\
Type: MS SQL Server\
Server: COMPUTER\SQLEXPRESS2008\
Database: REPOSITORY\
User: sa

## Global Variables Tab

Global Variables are used to replace Variable with Value, for example before SQL is executed <CustomerId> is be replaced with 1

EG

```sql
Select * from Customers where CustomerId =<CustomerId>
```

Is changed to

```sql
Select * from Customers where CustomerId =1
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/options/global-variables.png" title="Global Variables" >}}

### Predefined variables

```
<username> OS user name
<computername>
<datetime>
```

## Notes

- All settings are stored in C:\ProgramData\ETL-Tools.com folder, which makes moving software to a different computer much easier.
- Options.ini holds designer user interface settings plus global variables values
- **Note:** List of variables is shared between all applications
- Connections.ini holds the list of all available repository connections
- **Note:** This list is shared between all applications
- DesktopConnection.ini this file holds the ETL Designer repository connection name
- ServerConnection.ini this file holds the Execution agent, Management console and Monitors repository connection name

## [Options List]({{<relref "docs/advanced-etl-processor/options-list" >}})

Detailed options list

## Video Tutorials

{{< youtube id="QDsw7aP4wlg" class="ratio ratio-16x9" >}}
\
{{< youtube id="QIeMSJosb5w" class="ratio ratio-16x9" >}}

{{< aetl >}}
