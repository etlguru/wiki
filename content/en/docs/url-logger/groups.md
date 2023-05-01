---
author: Mike Rewnick
title: Groups
description: URL Logger Groups
draft: false
tags: ['URL Logger', 'Event Loggers']
date: 2022-04-03
menu: url-logger
group: url-logger
layout: docs
---

## Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

## Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into URL Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart URL Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart URL Logger

{{< url-logger >}}
