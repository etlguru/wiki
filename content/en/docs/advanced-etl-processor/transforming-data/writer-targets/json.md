---
author: Peter Jonson
title: JSON Writer
description: JSON Writer
draft: false
tags: ['Writer', 'JSON']
date: 2022-09-17

group: advanced-etl-processor-enterprise-writer
menu: advanced-etl-processor-enterprise
layout: docs
---

## About JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate. It is based on a subset of the JavaScript Programming Language, Standard ECMA-262 3rd Edition - December 1999.

http://www.json.org

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/target_is_json.png" title="Target Is JSON" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/target_is_json_file.png" title="Target Is JSON file" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/writer/target_is_json_format.png" title="Target Is JSON file" >}}

## JSON Examples

### Without root node

```json
[
  { "name": "id", "label": "id" },
  { "name": "email", "label": "EMail" },
  { "name": "ip", "label": "IP" },
  { "name": "logged_in", "label": "Logged In" }
]
```

### With root node

```json
{
 "root":
   {  "name": "id", "label": "id"	},
   {  "name": "email", "label": "EMail"},
   {  "name": "ip", "label": "IP"	},
   {  "name": "logged_in", "label": "Logged In" }
]
}
```

{{< aetl >}}
