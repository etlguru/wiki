---
author: Maria Salter
title: Automate sending HTML emails
description: Learn how to automate sending HTML emails
draft: false
tags: ['Knowledgebase', 'SMTP', 'Email', 'Automation']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

There two ways of sending HTML emails by using the package or as part as transformation

## Example

Sending price list to the customers

{{< image class="mx-auto d-block"  src="/images/knowledgebase/email-automation.png" title="Sending price list to the customers" >}}

## HTML Email

Enabling support for HTML email is easy: just tick a checkbox

{{< image class="mx-auto d-block"  src="/images/knowledgebase/send-email-action.png" title="HTML Email" >}}

## HTML Editor

{{< image class="mx-auto d-block"  src="/images/knowledgebase/send-email-action-htm-editor.png" title="HTML Editor" >}}

## Transformation

More advanced way of sending emails is using transformation

- Anything can be used as a data source to send emails files tables or databases
- It is possible to send multiple emails in one go
- Complex transformations can be performed on the data before sending it

{{< image class="mx-auto d-block"  src="/images/knowledgebase/email-transformation.png" title="Transformation" >}}

{{< aetl >}}
