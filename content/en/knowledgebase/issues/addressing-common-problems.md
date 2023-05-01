---
author: Maria Salter
title: Addressing common issues
description: Addressing common issues
draft: false
tags: ['Knowledgebase', 'Issues']
group: knowledgebase-issues
layout: docs
date: 2022-04-13
---

**Question:** I have just created a brand new repository but I can't figure out how to create transformation/package/report.

**Answer:** You have to create a transformation group first then you will be able to create transformation. If you have already got a transformation group right click on it and select new.

**Question:** I have opened existing transformation and unable to change connection details. Server name and other details are disabled.

**Answer:** You have to find a connection within objects tree on the left and change it there.

**Question:** I am reading data from blob field but it is empty

**Answer:** Please read the following article
[Blob Field is empty]({{<ref "blob-field-is-empty" >}})

**Question:** I am loading data into MS SQL Server but I am getting "Function sequence error"

**Answer:** Most likely your SQL server drivers too old.Please read the following article
[Function sequence error]({{<ref "function-sequence-error" >}})

I am reading data from MS SQL Server but I am getting "Invalid Descriptor Index"

**Answer:** Please read the following article:
[Invalid Descriptor Index]({{<ref "invalid-descriptor-index" >}})

**Question:** I have created transformation/import and I am able to execute it. But when I run it from the package it fails

**Answer:** Please read the following article:[Could not find any files to read]({{<ref "could-not-find-any-files-to-read" >}})

## Useful links

- [Things to avoid while designing data transformations]({{<ref "things-to-avoid-while-designing-data-transformations" >}})
- [Best practice for calculations]({{<ref "best-practice-for-calculations" >}})
- [Understanding Scheduler]({{<relref "/knowledgebase/tips/understanding-scheduler" >}})
- [Using Variables]({{<ref "using-variables" >}})

We have a lot of youtube videos, watch them, they are here for you

[Youtube tutorials](https://www.youtube.com/channel/UCvfiLK8W26L9PqUYaohcWZQ)

{{< aetl >}}
