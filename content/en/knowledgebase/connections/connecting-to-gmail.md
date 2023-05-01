---
author: Maria Salter
title: Connecting to GMail
description: This Article describes how to connect to Google Mail
draft: false
tags: ['Knowledgebase', 'Connection', 'GMail', 'EMail']
date: 2023-03-13
group: knowledgebase-connections
layout: docs
---

Please use the following link to check if Less Secured Apps are enabled
https://myaccount.google.com/security

{{< image class="mx-auto d-block"  src="/images/knowledgebase/less-secure-app-access.png" title="Less Secure APP Sccess" >}}

## SMTP Settings

{{< image class="mx-auto d-block"  src="/images/knowledgebase/gmail-smtp.png" title="Gmail SMTP" >}}

- SMTP Host: smtp.gmail.com
- SMTP Port: 587
- TLS Protocol: Require TLS
- SMTP Username: (your Gmail username)
- SMTP Password: (your Gmail password)

Still no luck? Check with your host if they have port 587 blocked by a firewall.

## POP3 Settings

{{< image class="mx-auto d-block"  src="/images/knowledgebase/gmail-pop3.png" title="Gmail POP3" >}}

- POP3 Host: pop.gmail.com
- POP3 Port: 995
- TLS Protocol: Explicit TLS
- POP3 Username: (your Gmail username)
- POP3 Password: (your Gmail password)

## IMAP4 Settings

{{< image class="mx-auto d-block"  src="/images/knowledgebase/gmail-imap4.png" title="Gmail IMAP4" >}}

- IMAP4 Host: imap.gmail.com
- IMAP4 Port: 993
- Encryption: Implicit TLS
- IMAP4 Username: (your Gmail username)
- IMAP4 Password: (your Gmail password)

### Less Secured Apps Enabled

When Less Secured Apps are disabled you can still access Gmail by using app passwords.

To create an app password make sure that two steps verification is enabled.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/two-steps-verification.png" title="Two Steps Verification" >}}

Click on app passwords and create a new one

{{< image class="mx-auto d-block"  src="/images/knowledgebase/app-password.png" title="APP Password" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/app-password2.png" title="APP Password" >}}
\
Use generated password to connect to Gmail

{{< aetl >}}
