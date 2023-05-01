---
author: Maria Salter
title: Groups
description: Active Table Editor Groups
draft: false
tags: ['Active Table Editor', 'Data Entry', 'Groups']
date: 2022-08-01
menu: active-table-editor
group: active-table-editor
layout: docs
---

[Active Table Editor](https://www.etl-tools.com/active-table-editor/overview.html) uses roles based security model. Every user must be a member of list one of the user's groups and have menu assigned. Combination of group access rights and user group membership defines the list of Menu Items user can get access to.

{{< image class="mx-auto d-block"  src="/images/active-table-editor/groups-grid.png" title="Group Grid" >}}
\
{{< image class="mx-auto d-block"  src="/images/active-table-editor/group-properties.png" title="Group Properties" >}}

## Creating a new User Group/Role

- Click Outlook bar
- Click Add
- Dialog box will appear
- Fill in Group Name you are about to create
- Click OK to finish the creation of a Group

Once Group is created it is possible to modify the list of Group members.

{{< image class="mx-auto d-block"  src="/images/active-table-editor/group-members-list.png" title="Group members list" >}}

## Access Rights

Access rights tabs define the list of objects available for group members.

{{< table "table-striped table-bordered" >}}

| Permission | Comments                                                      |
| ---------- | ------------------------------------------------------------- |
| No Access  | Blocks access to the Menu Item regardless of group membership |
| View       | Group members can view the data                               |
| Insert     | Group members can insert records                              |
| Update     | Group members can update records                              |
| Delete     | Group members can delete records                              |

{{< /table >}}

{{< image class="mx-auto d-block"  src="/images/active-table-editor/group-access-rights.png" title="Group access rights" >}}
\
{{< alert color="secondary" >}}
**Hint:** To add several objects hold the ctrl or shift key and select objects using the mouse.
{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/active-table-editor/add-documents.png" title="Add several objects" >}}

## Video Tutorial

{{< youtube  id="_J4rMCoLNxE" class="ratio ratio-16x9" >}}

{{< ate >}}
