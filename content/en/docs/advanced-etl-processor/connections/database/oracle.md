---
author: Peter Jonson
title: Oracle Connection
description: Oracle Database Connection
draft: false
tags: ['Connection', 'Database', 'Oracle']
date: 2023-07-05
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

For an Oracle connection, you will need to specify the TNS name required and provide the user name and password for the connection.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/oracle-connection.png" title="Oracle Connection" >}}
\
{{< alert color="secondary">}}It is also possible to use Oracle instant client syntax: servername:1521/ORCL{{< /alert >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/oracle-connection-comments.png" title="Oracle Connection Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/oracle-connection-user-fields.png" title="Oracle Connection User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

## Creating New Connection

- In the Name Text Box type in a new name for the connection you are about to create
- Select a TNS Name from the Server drop-down list or enter it manually
- Fill in Username/Password for the database you wish to connect to
- Click Test to ensure the details you have provided are correct
- Click OK to close the connection properties window

{{< alert color="secondary">}}If you are unsure of these parameters, please contact your Database Administrator for the correct settings.{{< /alert >}}

{{< aetl >}}
