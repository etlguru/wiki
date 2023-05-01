---
author: Mike Rewnick
title: Security
description: MQTT Logger Security
draft: false
tags: ['MQTT Logger', 'Security']
date: 2022-04-17
menu: mqtt-logger
group: mqtt-logger
layout: docs
---

There are two ways of running the MQTT Logger with security enabled or disabled.\
When security is disabled every one has unlimited access to MQTT Logger, We do not recommend running MQTT Logger with disabled security

{{< image class="mx-auto d-block"  src="/images/licensing-server/settings.png" title="Settings" >}}

## Login screen

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png" title="Login" >}}

## Security is enabled

{{< image class="mx-auto d-block"  src="/images/event-loggers/hl7-logger/hl7-logger-security-enabled.png" title="Security is enabled" >}}

## Security is disabled

{{< image class="mx-auto d-block"  src="/images/event-loggers/hl7-logger/hl7-logger-security-disabled.png" title="Security is disabled" >}}

## Password Encryption

The passwords are encrypted using a security key. We recommend changing it immediately after installation

The procedure is as follows

- Disable security
- Update security key
- Restart the logger
- Update users passwords
- Enable security
- Restart the logger

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

C:\ProgramData\ETL-Tools.com\mqtt-logger\

### Linux

/etc/etl-tools.com/mqtt-logger

{{< mqtt-logger >}}
