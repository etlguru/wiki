---
author: Mike Rewnick
title: Groups
description: MQTT Logger Groups
draft: false
tags: ['MQTT Logger', 'Groups']
date: 2022-04-17
menu: mqtt-logger
group: mqtt-logger
layout: docs
---

## Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

## Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}

**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into MQTT Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart MQTT Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart MQTT Logger

{{< mqtt-logger >}}
