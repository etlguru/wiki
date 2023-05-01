---
author: Peter Jonson
title: FTP Action
description: The Ftp Action performs various operations on the FTP server.
draft: false
tags: ['Package', 'Action', 'FTP', 'SFTP', 'FTPES', 'Download', 'Upload']
date: 2022-05-06

group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

The Ftp Action performs various operations on the FTP server.

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/ftp-action-workflow-1.png" title="Workflow tab" >}}

## Advanced tab

Click connect to view the storage content, buttons on the right allows to perform download, upload directory creation and delete operation.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/ftp-action-advanced-2.png" title="Advanced tab" >}}
\
{{< alert color="secondary">}}Enable logging option does not work for SFTP servers{{< /alert >}}

### Multiple files rename

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/ftp-action-rename-3.png" title="Multiple files rename" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/ftp-action-variables.png" title="After execution tab" >}}
Note: Ftp error message is stored in /<Ftp Error> variable

## Directory listing format

- Permissions
- File Size (if present)
- File Modification Date (if present)
- File/Directory Name

{{< alert color="secondary">}}The file is tab-delimited with no headers{{< /alert >}}

{{< aetl >}}
