---
author: Mike Rewnick
title: Groups
description: RabbitMQ Logger Groups
draft: false
tags: ['RabbitMQ Logger', 'Event Loggers']
date: 2022-05-19
menu: rabbitmq-logger
group: rabbitmq-logger
layout: docs
---

## Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

## Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into RabbitMQ Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart RabbitMQ Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart RabbitMQ Logger

{{< rabbitmq-logger >}}
