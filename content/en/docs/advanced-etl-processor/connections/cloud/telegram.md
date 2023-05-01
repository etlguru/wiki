---
author: Peter Jonson
title: Telegram Connection
description: Telegram Connection
draft: false
tags: ['Connection', 'Cloud', 'Telegram']
date: 2022-11-14

group: 'advanced-etl-processor-enterprise-cloud-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

## About Telegram

Telegram is a cloud-based instant messaging and voice over IP service. Telegram client apps are available for Android, iOS, Windows Phone, Windows NT, macOS and Linux. Users can send messages and exchange photos, videos, stickers, audio and files of any type.

Telegram's client-side code is open-source software but the source code for recent versions is not always immediately published, whereas its server-side code is closed-source and proprietary. The service also provides APIs to independent developers. In March 2018, Telegram stated that it had 200 million monthly active users.

Messages and media in Telegram are encrypted when stored on its servers, and client-server communication is also encrypted. The service provides end-to-end encryption for voice calls, and optional end-to-end encrypted "secret" chats between two online users, yet not for groups or channels.

Source [https://en.wikipedia.org/wiki/Telegram\_(software)](Wikipedia)

## ETL Integration

Our ETL software uses BOT API to process and send a Telegram message.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/cloud/telegram-connection.png" title="Telegram Connection" >}}
\
Use Botfather to create a new Telegram bot as described here
https://core.telegram.org/bots#6-botfather

{{< aetl >}}
