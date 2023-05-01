---
author: Peter Jonson
title: Azure Blob Action
description: Azure Blob Action provides an easy way of working with Azure Blob storage. Files can be uploaded, downloaded or deleted, it is also possible to work with containers or create a list of files
draft: false
tags: ['Package', 'Action', 'Azure', 'Blob']
date: 2023-03-18

group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

Azure Blob Action provides an easy way of working with Azure Blob storage. Files can be uploaded, downloaded or deleted, it is also possible to work with containers or create a list of files

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/azure-blob-action-properties-1.png" title="Workflow tab" >}}

## Advanced tab

Click connect to view the storage content, buttons on the right allows to perform the download, upload, container creation and delete operation.
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/azure-blob-action-properties-2.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/azure-blob-action-properties-3.png" title="After execution tab" >}}
\
{{< alert color="secondary">}}The Blob service is based on a flat storage scheme, not a hierarchical scheme. However, you may specify a character or string delimiter within a blob name to create a virtual hierarchy. For example, the following list shows valid and unique blob names.{{< /alert >}}

```
/virtualdirectory

/virtualdirectory/data.txt
```

Notice that a string can be valid as both a blob name and as a virtual directory name in the same container:

[More information](https://docs.microsoft.com/en-us/rest/api/storageservices/naming-and-referencing-containers--blobs--and-metadata)

To upload a file into virtual directory enter directory name after container name

## Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/azure-blob-action-properties.png" title="Azure Blob Action Properties" >}}

{{< aetl >}}
