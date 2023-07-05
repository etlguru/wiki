---
author: Peter Jonson
title: JDBC Connection
description: JDBC Database Connection
draft: false
tags: ['Connection', 'Database', 'JDBC']
group: 'advanced-etl-processor-enterprise-database-connections'
menu: advanced-etl-processor-enterprise
date: 2023-07-05
layout: docs
---

## About JDBC

JDBC is a Java-based data access technology (Java Standard Edition platform) which was created by Sun Microsystems, Inc.. It is an acronym as it is unofficially referred to as Java Database Connectivity, with DB being universally recognized as the abbreviation for database. This technology is an API for the Java programming language that defines how a client may access a database. It provides methods for querying and updating data in a database. JDBC is oriented towards relational databases. A JDBC-to-ODBC bridge enables connections to any ODBC-accessible data source in the JVM host environment.

Source: Wikipedia.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/jdbc.png" title="JDBC Connection" >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/jdbc-connection-comments.png" title="JDBC Connection Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/jdbc-connection-user-fields.png" title="JDBC Connection User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

## Notes

- SQL builder does not work with JDBC connections.
- List of JDBC drivers can be found here https://developers.sun.com/product/jdbc/drivers

{{< aetl >}}
