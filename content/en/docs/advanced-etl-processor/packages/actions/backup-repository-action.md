---
author: Peter Jonson
title: Backup Repository Action
description: Regular backup is a necessary action to protect the business from data loss.
draft: false
tags: ['Package', 'Action', 'Backup', 'Repository']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

## Importance of Backup

Regular backup is a necessary action to protect the business from data loss.

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/backup-repository-action.png" title="Backup Repository Action" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/backup-repository-variables.png" title="Backup Repository Variables" >}}

## About backup

Backup is a zip file which has sqlite database inside and ReadMe.txt file with a metadata about backup.

## ReadMe.txt Example

```
Repository Backup
Repository Name: SQL_SERVER
Repository Type: MS Sql Server
Repository Server: DBSLAMD\SQLEXPRESS2019
Repository Database: AETL_REPOSITORY
Created: 05/04/2023 09:47:12
Computer Name: DBSLAMD
User Name: dbsl
Application: AdvancedETLEnt.exe
Version: 6.3.10.0

www.etl-tools.com
```

## Performance

For very large repository it might take a while to perform backup. In this case we recommend clearing QUEU\\\* tables

{{< aetl >}}
