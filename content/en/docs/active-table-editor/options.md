---
author: Maria Salter
title: Options
description: Active Table Editor Options
draft: false
tags: ['Active Table Editor', 'Data Entry', 'Options']
date: 2022-09-17
menu: active-table-editor
group: active-table-editor
layout: docs
---

## Changing Active Table Editor Settings

- Click **System Menu**-> **File**-> **Options**
- Dialog box will appear

{{< image class="mx-auto d-block"  src="/images/active-table-editor/options-repository-connection.png" title="Repository Connection" >}}
\
{{< image class="mx-auto d-block"  src="/images/active-table-editor/repository-connection-options.png" title="Connection Options" >}}
\
{{< image class="mx-auto d-block"  src="/images/active-table-editor/options-user-options.png" title="Options" >}}
\
{{< image class="mx-auto d-block"  src="/images/active-table-editor/options-admin-options.png" title="Options" >}}

## Global Variables

**Global Variables** are used to replace Variable with Value, for example before input form is shown to the user `<CustomerId>` will be replaced with 1

**EG**

```sql
Select * from Customers where CustomerId = <CustomerId>
```

Is changed to

```sql
Select * from Customers where CustomerId = 1
```

{{< image class="mx-auto d-block"  src="/images/active-table-editor/options-global-variables.png" title="Global Variables" >}}

## Predefined variables

- `<ATEUserName>`
- `<username>` OS user name
- `<computername>`
- `<datetime>`

{{< alert color="secondary" >}}
**Note:** Works only with input forms SQL.
{{< /alert >}}

{{< ate >}}
