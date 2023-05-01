---
author: Maria Salter
title: Connecting to Microsoft Email Servers
description: This article describes how to connect to Microsoft Email Servers
draft: false
tags: ['Knowledgebase', 'Connection', 'Microsoft', 'Email', 'Office365', 'Outlook', 'hotmail', 'live.com']
date: 2023-03-14
group: knowledgebase-connections
layout: docs
---

## Two-step verification Enabled

Please use the following link to check if Two-step verification is enabled

https://account.live.com/proofs/manage/additional

{{< image class="mx-auto d-block"  src="/images/knowledgebase/microsoft-two-step-verification-1.png" title="Microsoft two step verification" >}}

If it is not enabled enable it and then click on app passwords and create a new one

{{< image class="mx-auto d-block"  src="/images/knowledgebase/microsoft-two-step-verification-2.png" title="Microsoft two step verification" >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/microsoft-two-step-verification-app-password.png" title="Microsoft two step verification password" >}}

### SMTP Settings

{{< image class="mx-auto d-block"  src="/images/knowledgebase/microsoft-smtp.png" title="SMTP Settings" >}}

- SMTP Host: smtp.office365.com
- SMTP Port: 587
- TLS Protocol: Explicit TLS
- SMTP Username: (your Microsoft email)
- SMTP Password: (your Application Password)

Still no luck? Check with your host if they have port 587 blocked by a firewall.

### POP3 Settings

{{< image class="mx-auto d-block"  src="/images/knowledgebase/microsoft-pop3.png" title="POP3 Settings" >}}

- POP3 Host: outlook.office365.com
- POP3 Port: 995
- TLS Protocol: Explicit TLS
- POP3 Username: (your Microsoft email)
- POP3 Password: (your Application Password)

### Enable POP access in Outlook.com

- If you want to use POP to access your email in Outlook.com, you'll first need to enable POP access.
- Select Settings Settings > View all Outlook settings > Mail > Sync email.
- Under POP and IMAP, select Yes under Let devices and apps use POP.
- Select Save.

### IMAP4 Settings

{{< image class="mx-auto d-block"  src="/images/knowledgebase/microsoft-imap4.png" title="IMAP4 Settings" >}}

- IMAP4 Host: outlook.office365.com
- IMAP4 Port: 993
- Encryption: Implicit TLS
- IMAP4 Username: (your Microsoft email)
- IMAP4 Password: (your Application Password)

## Two-step verification Disabled

When Two-step verification is disabled you can still access Microsoft email by using an ordinary password.

## How to register your app for Office 365 with OAuth 2.0 authentication

https://blog.rebex.net/registering-app-for-oauth2-office365#:~:text=How%20to%20register%20your%20app%20for%20Office365%20with,in%20the%20left%20menu%2C%20click%20%22App%20registrations%22.%20

{{< aetl >}}
