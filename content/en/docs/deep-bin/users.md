---
author: Mike Rewnick
title: Users
description: Deep Bin Users
draft: false
tags: ['Deep Bin', 'Users']
date: 2022-04-21
menu: deep-bin
group: deep-bin
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

It is possible to delete all users or disable them by accident. In this case, it might not be possible to login into Deep Bin

Follow these steps to recover

- Set ENABLE_SECURITY=0
- Restart Deep Bin
- Recreate/Enable users
- Set ENABLE_SECURITY=1
- Restart Deep Bin

{{< deep-bin >}}
