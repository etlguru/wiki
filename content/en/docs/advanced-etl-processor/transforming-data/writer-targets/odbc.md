---
author: Peter Jonson
title: ODBC Writer
description: Office365 Writer
draft: false
tags: ['Writer', 'Office365', 'EMail', 'ODBC']
date: 2022-11-20
group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

**About ODBC**

ODBC provides a standard software API method for accessing both relational and non-relational DBMS. It was developed by the SQL Access Group in 1992 in order to facilitate easier communication between applications and databases across computing platforms. Prior to its creation, if an application needed the ability to communicate with more than a single database, it would have to support and maintain an interface for each. ODBC provides a universal middleware layer between the application and DBMS, allowing the application developers to only have to learn a single interface, nor do they have to update their software if changes are made to the DBMS specification, only the driver needs updating. An ODBC driver can thus be thought of as analogous to a printer or other driver, providing a standard set of calls for the application to use, which then translates those commands into the correct commands at the DBMS end.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/odbc.png" title="ODBC" >}}
\
When Commit is set to “every statement” import works as follows:

```
Execute SQL before statement
Commit
Insert one record
Commit
Insert one record
Commit
Execute SQL after statement
Commit
```

**Note:**

Most databases support this way of loading data including files

When Commit is set to “once import is completed” import is executed inside one big transaction:

```
Start transaction
Execute SQL before statement
Insert one record
Insert one record
More inserts
Execute SQL after statement
Commit transaction
```

Not all databases support this way of loading data.

[List of ODBC Drivers Download Links]({{<relref "/knowledgebase/tips/list-of-odbc-drivers-download-links" >}})

{{< aetl >}}
