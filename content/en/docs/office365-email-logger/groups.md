---
author: Mike Rewnick
title: Groups
description: Office365 Email Logger Groups
draft: false
tags: ['Office365 Email Logger', 'Groups']
date: 2022-04-10
menu: office365-email-logger
group: office365-email-logger
layout: docs
---

## Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

## Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into IMAP4 Email Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart Office365 Email Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart Office365 Email Logger

{{< office365-email-logger >}}
