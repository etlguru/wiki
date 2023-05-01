---
author: Peter Jonson
title: Ole DB Writer
description: Ole DB Writer
draft: false
tags: ['Writer', 'OleDB']
date: 2022-09-17

group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/oledb.png" title="Ole DB Writer" >}}
\
{{< alert color="secondary" >}}
Ole DB is one of the slowest ways to extract the data and it uses a lot of memory.
{{< /alert >}}

**About OLE DB**

OLE DB (Object Linking and Embedding, Database, sometimes written as OLEDB or OLE-DB) is an API designed by Microsoft for accessing data from a variety of sources in a uniform manner. It is a set of interfaces implemented using the Component Object Model (COM); it is otherwise unrelated to OLE. It was designed as a higher-level replacement for, and successor to, ODBC, extending its feature set to support a wider variety of non-relational databases, such as object databases and spreadsheets that do not necessarily implement SQL.

OLE DB separates the data store from the application that needs access to it through a set of abstractions that include the datasource, session, command, and rowsets. This was done because different applications need access to different types and sources of data, and do not necessarily want to know how to access functionality with technology-specific methods. OLE DB is conceptually divided into consumers and providers. The consumers are the applications that need access to the data, and the providers are the software components that implement the interface and thereby provide the data to the consumer.

{{< aetl >}}
