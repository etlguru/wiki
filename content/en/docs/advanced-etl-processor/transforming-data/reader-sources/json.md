---
author: Peter Jonson
title: JSON Reader
description: JSON Reader
draft: false
tags: ['Reader', 'JSON']
date: 2022-09-17
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate. It is based on a subset of the JavaScript Programming Language, Standard ECMA-262 3rd Edition - December 1999.

https://www.json.org/json-en.html

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/json.png" title="JSON" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/json_grid.png" title="JSON Grid" >}}

## JSON Examples

### Without root node

```json
[
  { "id": 1, "Name": "John", "age": 25 },
  { "id": 2, "Name": "Maria", "age": 43 }
]
```

### With root node

```json
{
 "root":
 { "id" : 1,"Name": "John", "age": 25 },
 { "id" : 2,"Name": "Maria", "age": 43 }
]
}
```

[JSON Transformation Functions]({{<relref "docs/advanced-etl-processor/transformation-functions/json" >}})
