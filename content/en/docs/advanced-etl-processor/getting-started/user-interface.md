---
author: Peter Jonson
title: User Interface
description: Advanced ETL Processor User Interface
draft: false
tags: ['Transforming Data', 'Introduction']
date: 2022-08-01
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
weight: 6000
layout: docs
---

Upon starting the [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) software, the user is presented with the main window. This is where users design data transformations and workflows.

## System Menu

The system menu allows the user to access the essential setting and tools.

## Main window

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/main-window.png" title="Main window" >}}

## Quick Access Tabs

The "Quick Access Tabs" gives the user easy access to various functions of the application:

The titles of the tabs are self-explanatory, the default tab is "design".

## Objects Tree Toolbar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/objects-tree-toolbar.png" title="Objects Tree Toolbar" >}}

1. Selected object properties
1. Refresh object tree
1. Create a new object
1. Delete selected object
1. Cut
1. Copy
1. Paste
1. Incremental Search
1. Expand selected tree node
1. Collapse selected tree node

## Objects Tree Description

The "Objects" tree lists the main categories for the provision of objects. For instance, the "Directories" category contains icons representing the location of files and related information belonging to an individual item. For example, by clicking on the "Excel Files" icon you will access the directory area where all the Excel files are stored for processing.

You may also find icons representing individual database connection services. For instance, you can see connections available for both MS SQL Server and Oracle.

Other object types include ODBC connections. You can see from the illustration that the DEMO system has been configured, and as a result, the ODBC connections created are listed in the objects tree. The Advanced ETL Processor provides the Objects tree so the users have easy access to the main objects.

## Objects Tree List

Below is a list of possible objects with the short descriptions:

| Icon                                                                                                         | Name                                       | Description                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/project-icon.png" >}}        | Projects                                   | Provides a way to group objects together                                                                                                                  |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/directories.png" >}}         | Directories                                | Defines path to flat files, Excel files, MS Access databases or DBF files                                                                                 |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/jdbc-icon.jpg" >}}           | JDBC Connection                            | Defines JDBC connection properties                                                                                                                        |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/sqlserverce-icon.png" >}}    | SQL Server CE Connection                   | Defines MS SQL Server CE connection properties                                                                                                            |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/sqlserver-icon.png" >}}      | SQL Server Connection                      | Defines MS SQL Server connection properties                                                                                                               |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/odbc-icon.png" >}}           | ODBC Connection                            | Defines ODBC connection properties                                                                                                                        |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/oracle-icon.png" >}}         | Oracle Connection                          | Defines Oracle connection properties                                                                                                                      |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/connections-icon.png" >}}    | Ole DB                                     | Defines Ole DB connection properties                                                                                                                      |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/mysql-icon.png" >}}          | MySQL                                      | Defines MySql connection properties                                                                                                                       |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/postgresql-icon.png" >}}     | PostgreSQL                                 | Defines PostgreSQL connection properties                                                                                                                  |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/sqlite-icon.png" >}}         | SQLite                                     | Defines SQLite connection properties                                                                                                                      |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/interbase-icon.png" >}}      | Interbase/Firebird                         | Defines Interbase/Firebird connection properties                                                                                                          |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/mongodb.png" >}}             | MongoDb                                    | Defines MongoDb connection properties                                                                                                                     |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/ftp-icon.png" >}}            | FTP Connection                             | Defines FTP Server connection properties                                                                                                                  |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/smtp-icon.png" >}}           | SMTP Connection                            | Defines SMTP connection properties                                                                                                                        |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/pop3-icon.png" >}}           | POP3 Connection                            | Defines POP3 server connection properties                                                                                                                 |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/imap4-icon.jpg" >}}          | IMAP4 Connection                           | Defines IMAP4 server connection properties                                                                                                                |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/salesforce-icon.jpg" >}}     | SalesForce                                 | Connection Defines SalesForce connection properties                                                                                                       |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/brightperl-icon.png" >}}     | BrightPearl                                | Connection Defines BrightPearl connection properties                                                                                                      |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/google-icon.png" >}}         | Google Spreadsheet Connection              | Defines Google Spreadsheet connection properties                                                                                                          |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/tcpip-server.png" >}}        | IP Socket Connection                       | Defines IP Socket connection properties                                                                                                                   |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/tableau16.png" >}}           | Tableau Connection                         | Defines Tableau connection properties                                                                                                                     |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/lookup-icon.png" >}}         | Lookups and Lookups Groups                 | Provides an easy access to user defined data entry screens                                                                                                |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/transformation-icon.png" >}} | Transformations and Transformations Groups | Provides a way of transferring data from one database/file into another together with complex transformation, validation, sorting and grouping operations |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/report-icon.png" >}}         | Reports and Reports Groups                 | Reports design                                                                                                                                            |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/sqlscript-icon.png" >}}      | SQL Scripts and Scripts Groups             | Defines SQL statements to perform against target Databases                                                                                                |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/smtp-icon.png" >}}           | Email templates and groups                 | Creates general email templates.                                                                                                                          |
| {{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/icons/package-icon.png" >}}        | Packages and packages groups               | Combines complex Actions together like Ftp downloads File operations, emails, Check files, SQL scripts and Transformations.                               |

## Objects Groups

The [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) also has the ability to group objects together into “groups”. The purpose of doing this is so that objects of a specific type can be viewed as a branch of the object tree. Whenever a new object is added it will be placed under the appropriate branch for its type.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/group-of-objects.png" title="Objects Groups" >}}

To create a new object group select the appropriate object type for example transformation and click “new”.
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/create-new-object-group.png" title="Create new object group" >}}

Depending on the object type, the appropriate dialogue will be presented. In this example, the Transformation Group has been selected. The dialogue, in this case, requests a description and comment about the object to be created. Some of the fields in a dialogue of this type will be mandatory and will, therefore, have to be entered. However, comments will be optional, and just provide the user with the ability to specify more detail about an object and what it does.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-properties.png" title="Transformation Properties" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-properties-comments.png" title="Transformation Comments" >}}

## Status Bar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/progressbar.png" title="Progressbar" >}}

1. Number of records
1. Number of errors
1. Records per second
1. Start Date time
1. Time Left
1. Progress bar

## Incremental Search

For large implementations, the incremental search is a very useful option.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/incremental-search-1.png" title="Incremental Search" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/incremental-search-2.png" title="Incremental Search" >}}

{{< alert color="secondary">}}To edit the object double click on the name{{< /alert >}}

[Replace String Wizard]({{<relref "docs/advanced-etl-processor/replace-string" >}})

## Video Tutorials

{{< youtube id="A1NGpaIyFIw" class="ratio ratio-16x9" >}}
\
{{< youtube id="XwuYq-Amp3c" class="ratio ratio-16x9" >}}

{{< aetl >}}
