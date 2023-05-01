---
author: Mike Rewnick
title: Security
description: Licensing Server Security
draft: false
tags: ['Licensing Server']
date: 2022-04-05
menu: licensing-server
group: licensing-server
layout: docs
---

There are two ways of running the licensing server with security enabled or disabled.\
When security is disabled every one has unlimited access to licensing server, We do not recommend running licensing server with disabled security

{{< image class="mx-auto d-block"  src="/images/licensing-server/settings.png" title="Settings" >}}

## Login screen

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png" title="Login" >}}

## Security is enabled

{{< image class="mx-auto d-block"  src="/images/event-loggers/imap4-email-logger/imap4-logger-security-enabled.png" title="Security is enabled" >}}

## Security is disabled

{{< image class="mx-auto d-block"  src="/images/event-loggers/imap4-email-logger/imap4-logger-security-disabled.png" title="Security is disabled" >}}

## Password Encryption

The passwords are encrypted using a security key. We recommend changing it immediately after installation

The procedure is as follows

- Disable security
- Update security key
- Restart the server
- Update users passwords
- Enable security
- Restart the server
  SSL Encryption

We recommend using SSL encryption for network communications

The procedure is as follows

- Generate SSL Certificate
- Copy server.key and server.cer into .env folder
- Enable SSL
- Restart the server

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

## ENV Folder

### Windows

C:\ProgramData\ETL-Tools.com\licensing-server\

### Linux

/etc/etl-tools.com/licensing-server

{{< ls >}}
