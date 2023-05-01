---
author: Mike Rewnick
title: Groups
description: IMAP4 EMail Logger Groups
draft: false
tags: ['IMAP4 EMail Logger', 'Groups']
date: 2022-04-07
menu: imap4-email-logger
group: imap4-email-logger
layout: docs
---

### Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

### Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into IMAP4 Email Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart IMAP4 Email Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart IMAP4 Email Logger

{{< imap4-email-logger >}}
