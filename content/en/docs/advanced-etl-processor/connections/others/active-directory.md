---
author: Peter Jonson
title: Active Directory Connection
description: Active Directory Connection
draft: false
tags: ['Connection', 'Active Directory']
date: 2022-09-17
group: advanced-etl-processor-enterprise-other-connections
menu: advanced-etl-processor-enterprise
layout: docs
---

## About

Active Directory is a directory service developed by Microsoft that is used to manage and organize network resources within a Windows domain network. It provides a centralized database for storing and managing information about network objects such as users, computers, groups, and organizational units (OUs).

Active Directory allows administrators to control access to network resources by assigning permissions and policies to individual users or groups. It provides authentication and authorization services, allowing users to log in to the network and access resources based on their assigned permissions.

Active Directory also supports a hierarchical structure, where objects are organized in a logical and manageable manner. This structure is based on the Domain-OU model, where domains represent administrative boundaries and OUs represent organizational units within those domains. This hierarchical structure helps in organizing and delegating administrative tasks within a network.

Active Directory offers various features and services, including user and group management, security and access control, centralized authentication, replication, and the ability to integrate with other directory services. It is widely used in enterprise environments and provides a scalable and robust solution for managing and securing network resources.

{{< alert color="secondary">}}Active Directory Connection is used to extract data from active directory{{< /alert >}}

## Properties

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/active-directory-connection.png" title="Active Directory Connection" >}}
\
{{< alert color="secondary">}}When no username/password are provided current user is used{{< /alert >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/active-directory-comments.png" title="Active Directory Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/active-directory-user-fields.png" title="Active Directory User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

{{< aetl >}}
