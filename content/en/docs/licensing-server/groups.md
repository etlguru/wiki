---
author: Mike Rewnick
title: Groups
description: Licensing Server User Groups
draft: false
tags: ['Licensing Server']
date: 2022-03-17
menu: licensing-server
group: licensing-server
layout: docs
---

### Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

### Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into licensing server

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart licensing server
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart licensing server

{{< ls >}}
