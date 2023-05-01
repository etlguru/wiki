---
author: Peter Jonson
title: JDBC Reader
description: JDBC Reader
draft: false
tags: ['Reader', 'JDBC']
date: 2022-09-17
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About JDBC

**JDBC** is a Java-based data access technology (Java Standard Edition platform) from Sun Microsystems, Inc.. It is an acronym as it is unofficially referred to as Java Database Connectivity, with DB being universally recognized as the abbreviation for database. This technology is an API for the Java programming language that defines how a client may access a database. It provides methods for querying and updating data in a database. JDBC is oriented towards relational databases. A JDBC-to-ODBC bridge enables connections to any ODBC-accessible data source in the JVM host environment.

Source: [Wikipedia](https://en.wikipedia.org/wiki/Java_Database_Connectivity)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/jdbc.png" title="JDBC Reader" >}}
\
{{< alert color="secondary" >}}
SQL builder does not work with JDBC connections.
{{< /alert >}}

List of JDBC drivers can be found here https://www.soapui.org/docs/jdbc/reference/jdbc-drivers/
