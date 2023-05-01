---
author: Peter Jonson
title: File Metadata Action
description: The File Metadata Action object provides detailed file information via variables.
draft: false
tags: ['Package', 'Action', 'File', 'Metadata']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

The File Metadata Action object provides detailed file information via variables.

- File Size
- File Creation Date
- File Modification Date
- File Last Access Date
- Read Only
- Archive
- Hidden
- In Use

{{< alert color="secondary">}}File Metadata Action works only with the single file it will fail if no files were found or multiple files were found{{< /alert >}}

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-metadata-action-1.png" title="Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-metadata-action-2.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-metadata-action-3.png" title="After execution tab" >}}

{{< aetl >}}
