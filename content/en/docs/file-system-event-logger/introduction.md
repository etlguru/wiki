---
author: Mike Rewnick
title: Introduction
description: File System Event Logger writes information about file system changes into the database.
draft: false
tags: ['File System Event Logger', 'Introduction']
date: 2022-04-17
layout: docs
menu: file-system-event-logger
group: file-system-event-logger
layout: docs
---

File System Event Logger writes information about file system changes into the database.

## Supported Events

- Add file
- Modify file
- Delete file
- Add folder
- Delete folder

## Usage Example

{{< image class="mx-auto d-block"  src="/images/event-loggers/file-system-logger/file-system-event-logger-data-flow.png"  title="File System Event Logger Usage Example" >}}
\
{{< alert color="secondary" >}}
File System Event Logger works on both Windows and Linux. Please contact us if you want to run File System Event Logger on a different OS. We will create a special build for you
{{< /alert >}}

{{< file-system-event-logger >}}
