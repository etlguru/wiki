---
author: Peter Jonson
title: Migration
description: Migration from Visual Importer ETL to Advanced ETL Processor
draft: false
tags: ['Migration']
date: 2022-08-01
group: visual-importer-etl-enterprise
menu: visual-importer-etl-enterprise
weight: 1000
layout: docs
---

{{< alert color="warning" >}}
It is not recommended to use MS Access as a repository in a production environment, it tends to get corrupted over time
{{< /alert >}}

1. Create repository backup (Just in Case)
2. Uninstall Visual Importer ETL
3. Install Advanced ETL Processor
4. Connect to the same repository

Both Professional and Enterprise Editions are use [repository]({{<relref "docs/advanced-etl-processor/repository-database" >}}) database to store data. The repository database structure is the same for both editions. Multiple users of our ETL software can connect to the same repository and share the data

{{< alert color="danger" >}}
**Visual importer ETL** is the first ETL software product we created.
Since then we have designed **[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)** which is fully compatible with it and has much more features.\
For all new users we recommend **[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)**
{{< /alert >}}

{{< vimpe >}}
