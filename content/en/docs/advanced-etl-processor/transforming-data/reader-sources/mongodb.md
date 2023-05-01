---
author: Peter Jonson
title: MongoDB Reader
description: MongoDB Reader
draft: false
tags: ['Reader', 'MongoDB']
date: 2023-01-05

group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About MongoDB

MongoDB is a source-available cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with optional schemas. MongoDB is developed by MongoDB Inc. and licensed under the Server Side Public License (SSPL) which is deemed non-free by several distributions. MongoDB is a member of the MACH Alliance.

Source: [Wikipedia](https://en.wikipedia.org/wiki/MongoDB)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/mongodb.png" title="MongoDB " >}}
\
{{< alert color="secondary" >}}
There are three ways of connecting to MongoDB: Direct, Via SSL and Via SSH
{{< /alert >}}

## Example

Running Queries against MongoDB

The following operation returns all the documents from the products collection where qty is greater than 25 and returns only the \_id, item and qty fields:

```
db.products.find( { qty: { $gt: 25 } }, { item: 1, qty: 1 } )
```

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/mariadb2.png" title="MongoDB " >}}

[More examples](https://docs.mongodb.com/manual/reference/method/db.collection.find/)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/mongodb3.png" title="MongoDB " >}}
