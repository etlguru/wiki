---
author: Peter Jonson
title: Directory
description: Directory (OS Path to files or folders)
draft: false
tags: ['wiki', 'data', 'directory']
date: 2015-06-12
group: advanced-etl-processor-enterprise-other-connections
menu: advanced-etl-processor-enterprise
layout: docs
---

If a new directory is required, selecting “New” on the new directory icon brings up the following dialogue:

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/directory-properties.png" title="Directory properties" >}}

The following steps are needed to create a directory:

- In the Name Text Box type in a new name for the directory you are about to create
- Fill in the Directory path you wish to load data from
- Click OK to close the directory Properties Window

{{< alert color="secondary">}}The user may change connection or directory properties at any time by double-clicking on it.{{< /alert >}}

It is also possible to use a sub-directory in the existing directory \<DirectoryName>\Subdirectory.

For example \<Buffer>\tmp will expand to:

C:\Program Files\DB Software Laboratory\Demo\Buffer\tmp

{{< alert color="danger">}}To avoid issues never use mapped drives, use the UNC path instead{{< /alert >}}

## Path builder

- Double click on directory selector (or file selector)
- Choose a directory from the list
- Double click on it
- The directory is added to the path

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/path-builder.png" title="Path builder" >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/directory-comments.png" title="Directory Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/directory-user-fields.png" title="Directory User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

## Video Tutorial

{{< youtube id="gf8CdeseFj0" class="ratio ratio-16x9" >}}

{{< aetl >}}
