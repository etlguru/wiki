---
author: Peter Jonson
title: MongoDB Connection
description: MongoDB Database Connection
draft: false
tags: ['Connection', 'Database', 'MongoDB']
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
date: 2023-07-05
layout: docs
---

## About MongoDB

MongoDB is a free and open-source cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with schemas. MongoDB is developed by MongoDB Inc., and is published under a combination of the GNU Affero General Public License and the Apache License.

Source: WikiPedia

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mongodb-connection.png" title="MongoDB Connection" >}}
\
 {{< alert color="secondary" >}}
There are three ways of connecting to MongoDB: Direct, Via SSL and Via SSH
{{< /alert >}}

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mongodb-connection1.png" title="MongoDB Connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mongodb-connection2.png" title="MongoDB Connection" >}}
\
{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/mongodb-connection3.png" title="MongoDB Connection" >}}

## Creating New Connection

- In the Name Text Box type in a new name for the connection you are about to create
- Select a Server Name from Server Drop Down List
- Select a Database Name from the Drop Down List
- Fill in the Username/Password for the database you wish to connect to
- Enter SSL/SSH connections details if necessary
- Click Test to ensure the details you have provided are correct
- Click OK to close the connection properties window

{{< alert color="secondary" >}}
There are three ways of connecting to MongoDB: Direct, Via SSL and Via SSH
{{< /alert >}}

{{< aetl >}}
