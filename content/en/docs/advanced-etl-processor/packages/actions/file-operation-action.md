---
author: Peter Jonson
title: File Operation Action
description: File Operation Package Action
draft: false
tags: ['Package', 'Action', 'File']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

This action supports a wide range of file operations

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-operation-action-0.png" title="Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-operation-action-1.png" title="Advanced tab" >}}
\
{{< alert color="secondary">}}Move file only works locally within one disk, to move files between computers copy than delete files.{{< /alert >}}

### Renaming multiple files

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-operation-action-2.png" title="Renaming multiple files" >}}

### Merge files

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/merge-options.png" title="Merge files" >}}

File1.txt is added to File2.txt

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/file-operation-action-variables.png" title="After execution tab" >}}

- [Dynamic File names]({{<relref "docs/advanced-etl-processor/dynamic-file-names" >}})

{{< aetl >}}
