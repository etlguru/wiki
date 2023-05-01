---
author: Mike Rewnick
title: Users
description: Office365 Email Logger Users
draft: false
tags: ['Office365 Email Logger', 'Users']
date: 2022-04-10
menu: office365-email-logger
group: office365-email-logger
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

It is possible to delete all users or disable them by accident. In this case, it might not be possible to login into Office365 Email Logger

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart Office365 Email Logger
- Recreate/Enable users
- Set ENABLE_SECURITY=1
- Restart Office365 Email Logger

{{< office365-email-logger >}}
