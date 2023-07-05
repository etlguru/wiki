---
author: Peter Jonson
title: Office 365 Connection
description: Office 365 Connection
draft: false
tags: ['Connection', 'Office365', 'Email', 'Message']
date: 2023-01-24
group: 'advanced-etl-processor-enterprise-email-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

## About Office 365 Connection

Office 365 Connection is used to send and receive emails using Microsoft Graph API

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/office365-connection.png" title="Office 365 Connection" >}}

## Creating New Connection

- In the Name Text Box type in a new name for the Office 365 Connection you are about to create
- Fill in the email address
- Fill in Application (Client ID)
- Fill in Directory (Tenant ID)
- Fill in Client Secret
- Test connection
- Select the folder to download email messages from
- Click OK to close the Office 365 Connection properties dialogues

{{< alert color="secondary">}}Ask your system administrator for connection details{{< /alert >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/office365-connection-comments.png" title="Office 365 Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/office365-connection-user-fields.png" title="Office 365 User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

## Access rights example

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/email/msgraph.png" title="Access rights example" >}}

**[How to register your app for Office 365 with OAuth 2.0 authentication](https://blog.rebex.net/registering-app-for-oauth2-office365#:~:text=How%20to%20register%20your%20app%20for%20Office365%20with,in%20the%20left%20menu%2C%20click%20%22App%20registrations%22.%20)**

{{< aetl >}}
