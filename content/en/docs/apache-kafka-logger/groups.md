---
author: Mike Rewnick
title: Groups
description: Apache Kafka Logger Groups
date: 2023-03-07
draft: false
tags: ['Apache Kafka Logger', 'Groups']
menu: apache-kafka-logger
group: apache-kafka-logger
layout: docs
---

## Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

## Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into Apache Kafka Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart Apache Kafka Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart Apache Kafka Logger

{{< apache-kafka-logger >}}
