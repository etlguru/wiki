---
author: Mike Rewnick
title: Execution Queue
description: IMAP4 EMail Logger Execution Queue
draft: false
tags: ['IMAP4 EMail Logger', 'Execution Queue']
date: '2022-04-07'
menu: imap4-email-logger
group: imap4-email-logger
layout: docs
---

Having too many connections open may lead to various problems such as timeouts or server overload. Execution Queue guarantees that only one connection is open at a time. The tasks are executed sequentially one after another

{{< image class="mx-auto d-block"  src="/images/event-loggers/imap4-email-logger/imap4-email-logger-queue.png" title="Execution Queue">}}

{{< imap4-email-logger >}}
