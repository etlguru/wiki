---
author: Mike Rewnick
title: Security
description: Deep Bin Security
draft: false
tags: ['Deep Bin', 'Security']
date: 2022-04-21
menu: deep-bin
group: deep-bin
layout: docs
---

There are two ways of running the Deep Bin with security enabled or disabled.\
When security is disabled every one has unlimited access to Deep Bin, We do not recommend running Deep Bin with disabled security

{{< image class="mx-auto d-block"  src="/images/licensing-server/settings.png" title="Settings" >}}

## Login screen

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png" title="Login" >}}

## Security is enabled

{{< image class="mx-auto d-block"  src="/images/event-loggers/apache-kafka-logger/apache-kafka-logger-security-enabled.png" title="Security is enabled" >}}

## Security is disabled

{{< image class="mx-auto d-block"  src="/images/event-loggers/apache-kafka-logger/apache-kafka-logger-security-disabled.png" title="Security is disabled" >}}

## Password Encryption

The passwords are encrypted using a security key. We recommend changing it immediately after installation

The procedure is as follows

- Disable security
- Update security key
- Restart the bin
- Update users passwords
- Enable security
- Restart the bin

## SSL Encryption

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

C:\ProgramData\ETL-Tools.com\deep-bin\

### Linux

/etc/etl-tools.com/deep-bin

{{< deep-bin >}}
