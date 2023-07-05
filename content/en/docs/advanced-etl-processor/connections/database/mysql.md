---
author: Peter Jonson
title: MySQL/MariaDB Connection
description: MySQL/MariaDB Database Connection
draft: false
tags: ['Connection', 'Database', 'MySQL', 'MariaDB']
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
date: 2023-07-05
layout: docs
---

## About MySQL

The MySQL® database has become the world's most popular open-source database because of its consistently fast performance, high reliability and ease of use. It's used on every continent -- Yes, even Antarctica! -- by individual Web developers as well as many of the world's largest and fastest-growing organizations to save time and money powering their high-volume Web sites, business-critical systems and packaged software -- including industry leaders such as Yahoo!, Alcatel-Lucent, Google, Nokia, YouTube, and Zappos.com.

## About MariaDB

MariaDB is a community-developed fork of the MySQL relational database management system intended to remain free under the GNU GPL. Development is led by some of the original developers of MySQL, who forked it due to concerns over its acquisition by Oracle Corporation. Contributors are required to share their copyright with the MariaDB Foundation.

Source: Wikipedia

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mysql.png" title="Creating MySQL/MariaDB Connection" >}}
\
{{< alert color="secondary" >}}
There are three ways of connecting to My SQL: Direct, Via SSL and Via SSH
{{< /alert >}}

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mysql1.png" title="Creating MySQL/MariaDB Connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mysql2.png" title="Creating MySQL/MariaDB Connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mysql3.png" title="Creating MySQL/MariaDB Connection" >}}

## Creating New Connection

- In the Name Text Box type in a new name for the connection you are about to create
- Type in the hostname
- Select a Database name from the drop-down List
- Select the appropriate connection port default is 3306
- Fill in the Username/Password for the database you wish to connect to
- Fill in SSL/SSH connection details if necessary
- Click Test Connection to ensure the details you have provided are correct
- Click OK to close the connection properties window

## Video Tutorial

{{< youtube id="OfocHpdHyLk" class="ratio ratio-16x9" >}}
\
{{< youtube id="3dNFyvG23gM" class="ratio ratio-16x9" >}}

{{< aetl >}}
