---
author: Mike Rewnick
title: Execution Queue
description: Office365 Email Logger Execution Queue
draft: false
tags: ['Office365 Email Logger', 'Execution Queue']
date: 2022-04-11
menu: office365-email-logger
group: office365-email-logger
layout: docs
---

Having too many connections open may lead to various problems such as timeouts or server overload. Execution Queue guarantees that only one connection is open at a time. The tasks are executed sequentially one after another

{{< image class="mx-auto d-block"  src="/images/event-loggers/office365-email-logger/office365-email-logger-queue.png" title="Execution Queue" >}}

{{< office365-email-logger >}}
