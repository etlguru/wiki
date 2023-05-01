---
author: Peter Jonson
title: Send Email Action
description: Send Email Package Action (Emails can be sent as Plain text or HTML)
draft: false
tags: ['Package', 'Action', 'SMTP', 'Email', 'Message']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

Emails can be sent as Plain text or HTML

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/send-email-action-workflow-1.png" title="Workflow tab" >}}

## Advanced tab

Fully functional HTML Editor with the ability to embed pictures

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/send-email-action-advanced-2.png" title="Advanced tab" >}}
\
Plain text emails

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/integrated-text-editor.png" title="Plain text emails" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/smtp-action-variables.png" title="After execution tab" >}}

Type \<last email> in ‘TO’ box to reply to the last sender

{{< alert color="secondary">}}Send email action support both SMTP and Microsoft Graph API{{< /alert >}}

{{< aetl >}}
