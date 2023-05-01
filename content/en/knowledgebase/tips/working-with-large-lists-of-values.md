---
author: Maria Salter
title: Working with a large lists of values
description: Validating data against large list of values
draft: false
tags: ['Knowledgebase', 'List', 'Lookup']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

[Advanced ETL Processor's](https://www.etl-tools.com/advanced-etl-processor/overview.html) **"Is In list"** validation function is used to check if a value exists in the database or file.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/validation-rules/in_list_validation_function.png" title="In List" >}}

But In some situations, it is not very efficient.

- The list of values can be too big and it would not possible to fit it into the memory.
- Pulling the entire lookup may take too much time
- We may want to process just 10 records but our lookup has millions of records

In this case, there is better alternative **"Is value in database"** and **"If value in database"** transformation functions

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_value_in_database.png" title="If Value in the database transformation function" >}}
\
The way it works is very simple: during execution **\<value>** is replaced with actual value If the number of records returned is more than zero it returns success otherwise failure

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transformation-functions/if_value_in_database_prop.png" title="If Value in the database transformation function properties" >}}

{{< aetl >}}
