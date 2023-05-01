---
author: Maria Salter
title: Could not find any files to read
description: This article describes how to fix Could not find any files to read
draft: false
tags: ['Knowledgebase', 'Error']
date: 2022-08-01
group: knowledgebase-issues
layout: docs
---

A lot of our new users confused about how Data-reader works.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/could-not-find-any-files-to-read-error.png" title="Data-reader Error" >}}

## There are two scenarios

### Designing and testing transformation

When designing a transformation the user can point the data reader at any file and process it.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/sourcefilec2.png" title="Source File" >}}
\
For example, the user is usually working with the file located on C: drive,
but later the user may want to see the file on the network drive.

That gives a user the flexibility to validate and process file(s) at any location

### Working with packages

However, when the transformation is run from the package the application will look for the file in the directory specified by the directory connection
If there is no such file the transformation will fail

{{< image class="mx-auto d-block"  src="/images/knowledgebase/directory3.png" title="Directory" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/reader4.png" title="Reader" >}}

That makes it easy to switch from one directory to another while working with multiple transformations

## Video Tutorial

{{< youtube id="EjH4IsNte7g" class="ratio ratio-16x9" >}}

{{< aetl >}}
