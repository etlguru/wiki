---
author: Peter Jonson
title: File System Reader
description: File System Reader
draft: false
tags: ['Reader', 'File System', 'Metadata']
date: 2022-08-01
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About

File System Reader loads content of entire file into memory so it can transformed as a whole

**It can be used to**

- to load files content into the database blob fields.
- to load file metadata information into the database.
- to transform file content (replace or delete string fro example)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/filesystem.png" title="Data Source is a File System" >}}
\
{{< alert color="secondary" >}}
It recommended exporting data once it loaded into the database for additional testing
{{< /alert >}}

**Table creation SQL script example for MS SQL Server**

```sql
create table FilesList
(
[Directory] [varchar](255) NULL,
[File Name] [varchar](255) NULL,
[Size] int,
[Created Date] datetime,
[Read Only] [varchar](6) NULL,
[Hidden] [varchar](6) NULL,
[Archive] [varchar](6) NULL,
[File Data] blob,
[Modified Date] datetime,
[Accessed Date] datetime
)
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/file-system-transformation.png" title="File System ,Directory" >}}

## Video Tutorial

{{< youtube id="-XiLUTdd2ic" class="ratio ratio-16x9" >}}
