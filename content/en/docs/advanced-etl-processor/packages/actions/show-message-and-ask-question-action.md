---
author: Peter Jonson
title: Show Message and Ask Question Action
description: Show Message and Ask Question Package Actions are used for debugging.
draft: false
tags: ['Package', 'Action', 'Question', 'Message']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

Show Message and Ask Question package actions are used for debugging.

- Ask Question does not work when the agent is used for execution or in a separate thread.
- When executed from the agent Show Message action writes the message into the log

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/show-message-and-ask-question-action-1.png" title="Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/show-message-and-ask-question-action-2.png" title="Advanced tab" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/ask-question.png" title="Advanced tab" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/show-message.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/ask-question-variables.png" title="After execution tab" >}}

{{< aetl >}}
