---
author: Mike Rewnick
title: Groups
description: HL7 Logger Groups
draft: false
tags: ['HL7 Event Logger', 'Groups']
date: 2022-04-17
menu: hl7-logger
group: hl7-logger
layout: docs
---

### Groups grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/groups-grid.png" title="Groups Grid" >}}

### Group form

{{< image class="mx-auto d-block"  src="/images/licensing-server/group-edit.png" title="Groups Form" >}}
\
**Note**

It is possible to delete all groups or disable them by accident. In this case, it might not be possible to login into HL7 Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart HL7 Logger
- Recreate/Enable groups
- Set ENABLE_SECURITY=1
- Restart HL7 Logger

{{< hl7-event-logger >}}
