---
author: Peter Jonson
title: Working with Filenames and Directories
description: Working with Filenames and Directories
draft: false
tags: ['Package', 'Action', 'Filenames', 'Directories']
date: 2022-09-17
group: advanced-etl-processor-enterprise-package
menu: advanced-etl-processor-enterprise
layout: docs
weight: 3
---

Consider the following scenarios.

- Every day we export data from our database and would like to save it into a different file using the current date as a part of the file.
- We would like to load yesterday’s data from the folder which has date part in the name

We can use functions in filenames to do it as follows

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-and-direct-1.png" title="Filenames and Directories" >}}

```
GETSYSTEMVARIABLE('SYSTEM_DATE')
```

will return current date in ‘YYYYMMDDHHNNSS’ format

If we want only part of the date we can use **LeftString(String,Count):String** for example

```
LeftString(GETSYSTEMVARIABLE('SYSTEM_DATE'),8)
```

will return only date part.

Now more complicated example for loading yesterday’s data;

```
LeftString(DecDateS(GETSYSTEMVARIABLE('SYSTEM_DATE'),'YYYYMMDDHHNNSS', 'DAY',1),8)
```

Another example:

```
C:\Data{GetSystemDate('YYYYMMDD')}.csv
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-and-direct-2.png" title="Filenames and Directories" >}}

For complete reference of available functions consult [Supported Functions List]({{<relref "docs/advanced-etl-processor/supported-functions-list" >}})

{{< alert color="secondary">}}Only one {} pair is allowed{{< /alert >}}

{{< aetl >}}
