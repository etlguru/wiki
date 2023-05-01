---
author: Peter Jonson
title: Oracle Writer
description: Oracle Writer
draft: false
tags: ['Writer', 'Oracle']
date: 2022-09-17
group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) supports four methods of loading data into oracle: Direct path load, Conventional path load, Ole DB and ODBC

Direct-path load in Oracle is used when a session is reading buffers from disk directly into the PGA(opposed to the buffer cache in SGA). During direct-path INSERT operations, the database appends the inserted data after existing data in the table. Data is written directly into data files, bypassing the buffer cache. Free space in the existing data is not reused, and referential integrity constraints are ignored. You may prefer to use a direct path load when you have a large amount of data to load quickly and you want to load data in parallel for maximum performance, but there are alternative costs to be aware of.

With the conventional path load method, arrays of rows are inserted with standard SQL INSERT statements; integrity constraints and insert triggers are automatically applied. But when you load data with the direct path, [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) disables some integrity constraints and all database triggers.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/oracle.png" title="Oracle" >}}

**Note:**

Option ‘Commit every Array’ works only for Oracle conventional path loading

**The constraints that remain in force are:**

- NOT NULL
- UNIQUE
- PRIMARY KEY (unique-constraints on not-null columns)

**The following constraints are automatically disabled by default:**

- CHECK constraints
- Referential constraints (FOREIGN KEY)

**For conventional path loading when Commit every Array is checked import works as follows:**

Execute SQL before statement\
Commit\
Insert Array of records \
Commit\
Insert Array of records\
Commit\
Execute SQL after statement\
Commit

**When Commit every Array is not checked import is executed inside one big transaction:**\

Start transaction\
Execute SQL before statement\
Insert Array of records\
Insert Array of records\
More inserts\
Execute SQL after statement\
Commit transaction

**Note:**

Loading Unicode data via direct path is not supported.
If your database was not created with Unicode support but you have some NCHAR
or NVARCHAR2 fields you may need to set array size to 1.

{{< aetl >}}
