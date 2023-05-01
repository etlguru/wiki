---
author: Mike Rewnick
title: Groups
description: File System Event Logger Groups
draft: false
tags: ['File System Event Logger', 'Groups']
date: 2022-04-05
menu: file-system-event-logger
group: file-system-event-logger
layout: docs
---

## Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

## Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into File System Event Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart File System Event Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart File System Event Logger

{{< file-system-event-logger >}}
