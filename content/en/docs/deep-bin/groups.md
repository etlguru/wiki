---
author: Mike Rewnick
title: Groups
description: Deep Bin users' groups (Roles).
draft: false
tags: ['Deep Bin', 'Groups']
date: 2022-04-21
menu: deep-bin
group: deep-bin
layout: docs
---

## Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

## Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}

**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into Deep Bin

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart Deep Bin
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart Deep Bin

{{< deep-bin >}}
