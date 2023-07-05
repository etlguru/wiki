---
author: Peter Jonson
title: IMAP4 Connection
description: IMAP4 Connection
draft: false
tags: ['Connection', 'IMAP4', 'Email', 'Message']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-email-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

## About IMAP4

Internet message access protocol (IMAP) is one of the two most prevalent Internet standard protocols for e-mail retrieval, the other being the Post Office Protocol (POP). Virtually all modern e-mail clients and mail servers support both protocols as a means of transferring e-mail messages from a server.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/imap4-connection-properties.png" title="IMAP4 Connection" >}}

## Creating New Connection

- In the Name Text Box type in a new name for the IMAP4 connection you are about to create
- Fill in host name
- Select TCP/IP port (default is 143)
- Type in user name and password
- Select folder
- Click OK to close the IMAP4 connection properties window

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/imap4-connection-comments.png" title="IMAP4 Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/imap4-connection-user-fields.png" title="IMAP4 User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

{{< aetl >}}
