---
author: Mike Rewnick
title: Users
description: HL7 Logger Users
draft: false
tags: ['HL7 Event Logger', 'Users']
date: 2022-04-17
menu: hl7-logger
group: hl7-logger
layout: docs
---

## Users grid

{{< image class="mx-auto d-block"  src="/images/licensing-server/users-grid.png" title="Users Grid" >}}

## User form

{{< image class="mx-auto d-block"  src="/images/licensing-server/user-edit.png" title="Users Form" >}}

## Changing User password

{{< image class="mx-auto d-block"  src="/images/licensing-server/change-user-password.png" title="Changing User password" >}}

## Changing Current User password

{{< image class="mx-auto d-block"  src="/images/licensing-server/change-my-password.png" title="Changing Current User password" >}}

## Changing Current User details

{{< image class="mx-auto d-block"  src="/images/licensing-server/my-details.png" title="Changing Current User details" >}}
\
**Note**

It is possible to delete all users or disable them by accident. In this case, it might not be possible to login into HL7 Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart HL7 Logger
- Recreate/Enable users
- Set ENABLE_SECURITY=1
- Restart HL7 Logger

{{< hl7-event-logger >}}
